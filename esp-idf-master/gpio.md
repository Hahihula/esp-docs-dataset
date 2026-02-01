---
original_file_path: api-reference/peripherals/gpio.rst
---

# GPIO & RTC GPIO

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## GPIO Summary

:::::: only
SOC_RTCIO_INPUT_OUTPUT_SUPPORTED

::: only
not SOC_LP_PERIPHERALS_SUPPORTED

There is also separate \"RTC GPIO\" support, which functions when GPIOs are routed to the \"RTC\" low-power and analog subsystem. These pin functions can be used when:
:::

::: only
SOC_LP_PERIPHERALS_SUPPORTED

There is also separate \"RTC GPIO\" support, which functions when GPIOs are routed to the \"RTC\" low-power, analog subsystem, and Low-Power(LP) peripherals. These pin functions can be used when:
:::

::: list
\- In Deep-sleep mode :SOC_ULP_FSM_SUPPORTED: - The `Ultra Low Power FSM co-processor <../../api-reference/system/ulp>`{.interpreted-text role="doc"} is running :SOC_RISCV_COPROC_SUPPORTED: - The `Ultra Low Power RISC-V co-processor <../../api-reference/system/ulp-risc-v>`{.interpreted-text role="doc"} is running :SOC_LP_CORE_SUPPORTED: - The `Ultra Low Power LP-Core co-processor <../../api-reference/system/ulp-lp-core>`{.interpreted-text role="doc"} is running - Analog functions such as ADC/DAC/etc are in use :SOC_LP_PERIPHERALS_SUPPORTED: - LP peripherals, such as LP_UART, LP_I2C, are in use
:::
::::::

## IO Configuration

An IO can be used in two ways:

- As a simple GPIO input to read the level on the pin, or as a simple GPIO output to output the desired level on the pin.
- As a peripheral signal input/output.

IDF peripheral drivers always take care of the necessary IO configurations that need to be applied onto the pins, so that they can be used as the peripheral signal inputs or outputs. This means the users usually only need to be responsible for configuring the IOs as simple inputs or outputs. `gpio_config`{.interpreted-text role="cpp:func"} is an all-in-one API that can be used to configure the I/O mode, internal pull-up/pull-down resistors, etc. for pins, including the ones reused by the USB PHY.

In some applications, an IO pin can serve dual purposes. For example, the IO, which outputs a LEDC PWM signal, can also act as a GPIO input to generate interrupts or GPIO ETM events. Careful handling on the configuration step is necessary for such dual use of IO pins cases. `gpio_config`{.interpreted-text role="cpp:func"} is an API that overwrites all the current configurations, so it must be called to set the pin mode to `gpio_mode_t::GPIO_MODE_INPUT`{.interpreted-text role="cpp:enumerator"} before calling the LEDC driver API which connects the output signal to the pin. As an alternative, if no other configuration is needed other than making the pin input enabled, `gpio_input_enable`{.interpreted-text role="cpp:func"} can be the one to call at any time to achieve the same purpose.

## Check Current Configuration of IOs

GPIO driver offers a dump function `gpio_dump_io_configuration`{.interpreted-text role="cpp:func"} to show the current configurations of IOs, such as pull-up/pull-down, input/output enable, pin mapping, etc. Below is an example of how to dump the configuration of GPIO4, GPIO18, and GPIO26:

    gpio_dump_io_configuration(stdout, (1ULL << 4) | (1ULL << 18) | (1ULL << 26));

The dump will be like this:

    ================IO DUMP Start================
    IO[4] -
      Pullup: 1, Pulldown: 0, DriveCap: 2
      InputEn: 1, OutputEn: 0, OpenDrain: 0
      FuncSel: 1 (GPIO)
      GPIO Matrix SigIn ID: (simple GPIO input)
      SleepSelEn: 1

    IO[18] -
      Pullup: 0, Pulldown: 0, DriveCap: 2
      InputEn: 0, OutputEn: 1, OpenDrain: 0
      FuncSel: 1 (GPIO)
      GPIO Matrix SigOut ID: 256 (simple GPIO output)
      SleepSelEn: 1

    IO[26] **RESERVED** -
      Pullup: 1, Pulldown: 0, DriveCap: 2
      InputEn: 1, OutputEn: 0, OpenDrain: 0
      FuncSel: 0 (IOMUX)
      SleepSelEn: 1

    =================IO DUMP End==================

In addition, if you would like to dump the configurations of all IOs, you can use:

    gpio_dump_io_configuration(stdout, SOC_GPIO_VALID_GPIO_MASK);

If an IO pin is routed to a peripheral signal through the GPIO matrix, the signal ID printed in the dump information is defined in the `soc/{IDF_TARGET_PATH_NAME}/include/soc/gpio_sig_map.h`{.interpreted-text role="component_file"} header file. The word `**RESERVED**` indicates the IO is occupied by either SPI flash or PSRAM. It is strongly not recommended to reconfigure them for other application purposes.

Do not rely on the default configurations values in the Technical Reference Manual, because it may be changed in the bootloader or application startup code before app_main.

:::::: only
SOC_GPIO_SUPPORT_PIN_GLITCH_FILTER or SOC_GPIO_FLEX_GLITCH_FILTER_NUM

## GPIO Glitch Filter

The {IDF_TARGET_NAME} chip features hardware filters to remove unwanted glitch pulses from the input GPIO, which can help reduce false triggering of the interrupt and prevent a noise being routed to the peripheral side.

::: only
SOC_GPIO_SUPPORT_PIN_GLITCH_FILTER

Each GPIO can be configured with a glitch filter, which can be used to filter out pulses shorter than **two** sample clock cycles. The duration of the filter is not configurable. The sample clock is the clock source of the IO_MUX. In the driver, we call this kind of filter as `pin glitch filter`. You can create the filter handle by calling `gpio_new_pin_glitch_filter`{.interpreted-text role="cpp:func"}. All the configurations for a pin glitch filter are listed in the `gpio_pin_glitch_filter_config_t`{.interpreted-text role="cpp:type"} structure.

- `gpio_pin_glitch_filter_config_t::gpio_num`{.interpreted-text role="cpp:member"} sets the GPIO number to enable the glitch filter.
:::

::: only
SOC_GPIO_FLEX_GLITCH_FILTER_NUM

{IDF_TARGET_FLEX_GLITCH_FILTER_NUM:default=\"8\"}

{IDF_TARGET_NAME} provides {IDF_TARGET_FLEX_GLITCH_FILTER_NUM} flexible glitch filters, whose duration is configurable. We refer to this kind of filter as `flex flitch filter`. Each of them can be applied to any input GPIO. However, applying multiple filters to the same GPIO does not make difference from one. You can create the filter handle by calling `gpio_new_flex_glitch_filter`{.interpreted-text role="cpp:func"}. All the configurations for a flexible glitch filter are listed in the `gpio_flex_glitch_filter_config_t`{.interpreted-text role="cpp:type"} structure.

- `gpio_flex_glitch_filter_config_t::gpio_num`{.interpreted-text role="cpp:member"} sets the GPIO that will be applied to the flex glitch filter.
- `gpio_flex_glitch_filter_config_t::window_width_ns`{.interpreted-text role="cpp:member"} and `gpio_flex_glitch_filter_config_t::window_thres_ns`{.interpreted-text role="cpp:member"} are the key parameters of the glitch filter. During `gpio_flex_glitch_filter_config_t::window_width_ns`{.interpreted-text role="cpp:member"}, any pulse whose width is shorter than `gpio_flex_glitch_filter_config_t::window_thres_ns`{.interpreted-text role="cpp:member"} will be discarded. Please note that, you can not set `gpio_flex_glitch_filter_config_t::window_thres_ns`{.interpreted-text role="cpp:member"} bigger than `gpio_flex_glitch_filter_config_t::window_width_ns`{.interpreted-text role="cpp:member"}.
:::

::: only
SOC_GPIO_SUPPORT_PIN_GLITCH_FILTER and SOC_GPIO_FLEX_GLITCH_FILTER_NUM

Please note, the `pin glitch filter` and `flex glitch filter` are independent. You can enable both of them for the same GPIO.
:::

The glitch filter is disabled by default, and can be enabled by calling `gpio_glitch_filter_enable`{.interpreted-text role="cpp:func"}. To recycle the filter, you can call `gpio_del_glitch_filter`{.interpreted-text role="cpp:func"}. Please note, before deleting the filter, you should disable it first by calling `gpio_glitch_filter_disable`{.interpreted-text role="cpp:func"}.
::::::

::::::: only
SOC_GPIO_SUPPORT_PIN_HYS_FILTER

## GPIO Hysteresis Filter

{IDF_TARGET_NAME} support the hardware hysteresis of the input pin, which can reduce the GPIO interrupt shoot by accident due to unstable sampling when the input voltage is near the criteria of logic 0 and 1, especially when the input logic level conversion is slow or the voltage setup time is too long.

::::: only
SOC_GPIO_SUPPORT_PIN_HYS_CTRL_BY_EFUSE

Each pin can enable hysteresis function independently. By default, it controlled by eFuse and been closed, but it can also be enabled or disabled by software manually. You can select the hysteresis control mode by configuring `gpio_config_t::hys_ctrl_mode`{.interpreted-text role="cpp:member"}. Hysteresis control mode is set along with all the other GPIO configurations in `gpio_config`{.interpreted-text role="cpp:func"}.

:::: note
::: title
Note
:::

When the hysteresis function is controlled by eFuse, this feature can still be controlled independently for each pin, you need to [burn the eFuse](https://docs.espressif.com/projects/esptool/en/latest/esp32/espefuse/index.html) to enable the hysteresis function on specific GPIO additionally.
::::
:::::

::: only
not SOC_GPIO_SUPPORT_PIN_HYS_CTRL_BY_EFUSE

Each pin can enable hysteresis function independently. By default, the function is not enabled. You can select the hysteresis control mode by configuring `gpio_config_t::hys_ctrl_mode`{.interpreted-text role="cpp:member"}. Hysteresis control mode is set along with all the other GPIO configurations in `gpio_config`{.interpreted-text role="cpp:func"}.
:::
:::::::

## Application Example

::: list
\* `peripherals/gpio/generic_gpio`{.interpreted-text role="example"} demonstrates how to configure GPIO to generate pulses and use it with interruption. :esp32s2: \* `peripherals/gpio/matrix_keyboard`{.interpreted-text role="example"} demonstrates how to drive a common matrix keyboard using the dedicated GPIO APIs, including manipulating the level on a group of GPIOs, triggering edge interrupt, and reading level on a group of GPIOs.
:::

## API Reference - Normal GPIO

::: include-build-file
inc/gpio.inc
:::

::: include-build-file
inc/gpio_types.inc
:::

:::::: only
SOC_RTCIO_INPUT_OUTPUT_SUPPORTED

## API Reference - RTC GPIO

::: include-build-file
inc/rtc_io.inc
:::

::: include-build-file
inc/lp_io.inc
:::

::: include-build-file
inc/rtc_io_types.inc
:::
::::::

:::: only
SOC_GPIO_SUPPORT_PIN_GLITCH_FILTER or SOC_GPIO_FLEX_GLITCH_FILTER_NUM

## API Reference - GPIO Glitch Filter

::: include-build-file
inc/gpio_filter.inc
:::
::::
