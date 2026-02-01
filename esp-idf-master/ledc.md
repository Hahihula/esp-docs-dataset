---
original_file_path: api-reference/peripherals/ledc.rst
---

# LED Control (LEDC)

{IDF_TARGET_LEDC_MAX_FADE_RANGE_NUM: default=\"1\", esp32c6=\"16\", esp32h2=\"16\", esp32p4=\"16\", esp32c5=\"16\", esp32c61=\"16\", esp32h21=\"16\"}

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Introduction

The LED control (LEDC) peripheral is primarily designed to control the intensity of LEDs, although it can also be used to generate PWM signals for other purposes. It has {IDF_TARGET_SOC_LEDC_CHANNEL_NUM} channels which can generate independent waveforms that can be used, for example, to drive RGB LED devices.

::: only
esp32

LEDC channels are divided into two groups of 8 channels each. One group of LEDC channels operates in high speed mode. This mode is implemented in hardware and offers automatic and glitch-free changing of the PWM duty cycle. The other group of channels operate in low speed mode, the PWM duty cycle must be changed by the driver in software. Each group of channels is also able to use different clock sources.
:::

The PWM controller can automatically increase or decrease the duty cycle gradually, allowing for fades without any processor interference.

## Functionality Overview

::: only
esp32

Setting up a channel of the LEDC in either `high or low speed mode <ledc-api-high_low_speed_mode>`{.interpreted-text role="ref"} is done in three steps:
:::

::: only
not esp32

Setting up a channel of the LEDC is done in three steps. Note that unlike ESP32, {IDF_TARGET_NAME} only supports configuring channels in \"low speed\" mode.
:::

1.  `ledc-api-configure-timer`{.interpreted-text role="ref"} by specifying the PWM signal\'s frequency and duty cycle resolution.
2.  `ledc-api-configure-channel`{.interpreted-text role="ref"} by associating it with the timer and GPIO to output the PWM signal.
3.  `ledc-api-change-pwm-signal`{.interpreted-text role="ref"} that drives the output in order to change LED\'s intensity. This can be done under the full control of software or with hardware fading functions.

As an optional step, it is also possible to set up an interrupt on fade end.

<figure class="align-center">
<img src="../../../_static/ledc-api-settings.jpg" alt="Key Settings of LED PWM Controller&#39;s API" />
<figcaption aria-hidden="true">Key Settings of LED PWM Controller's API</figcaption>
</figure>

:::: note
::: title
Note
:::

For an initial setup, it is recommended to configure for the timers first (by calling `ledc_timer_config`{.interpreted-text role="cpp:func"}), and then for the channels (by calling `ledc_channel_config`{.interpreted-text role="cpp:func"}). This ensures the PWM frequency is at the desired value since the appearance of the PWM signal from the IO pad.
::::

### Timer Configuration {#ledc-api-configure-timer}

Setting the timer is done by calling the function `ledc_timer_config`{.interpreted-text role="cpp:func"} and passing the data structure `ledc_timer_config_t`{.interpreted-text role="cpp:type"} that contains the following configuration settings:

::: list

esp32

:   - Speed mode `ledc_mode_t`{.interpreted-text role="cpp:type"}

not esp32

:   - Speed mode (value must be `LEDC_LOW_SPEED_MODE`)

- Timer number `ledc_timer_t`{.interpreted-text role="cpp:type"}
- PWM signal frequency in Hz
- Resolution of PWM duty
- Source clock `ledc_clk_cfg_t`{.interpreted-text role="cpp:type"}
:::

The frequency and the duty resolution are interdependent. The higher the PWM frequency, the lower the duty resolution which is available, and vice versa. This relationship might be important if you are planning to use this API for purposes other than changing the intensity of LEDs. For more details, see Section `ledc-api-supported-range-frequency-duty-resolution`{.interpreted-text role="ref"}.

The source clock can also limit the PWM frequency. The higher the source clock frequency, the higher the maximum PWM frequency can be configured.

::: only
esp32

  ------------------------------------------------------------------------------------------------------
  Clock name    Clock freq   Speed mode   Clock capabilities
  ------------- ------------ ------------ --------------------------------------------------------------
  APB_CLK       80 MHz       High / Low   /

  REF_TICK      1 MHz        High / Low   Dynamic Frequency Scaling compatible

  RC_FAST_CLK   \~ 8 MHz     Low          Dynamic Frequency Scaling compatible, Light-sleep compatible
  ------------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::: only
esp32s2

  --------------------------------------------------------------------------------------------------
  Clock name        Clock freq        Clock capabilities
  ----------------- ----------------- --------------------------------------------------------------
  APB_CLK           80 MHz            /

  REF_TICK          1 MHz             Dynamic Frequency Scaling compatible

  RC_FAST_CLK       \~ 8 MHz          Dynamic Frequency Scaling compatible, Light-sleep compatible

  XTAL_CLK          40 MHz            Dynamic Frequency Scaling compatible
  --------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::: only
esp32s3 or esp32c3

  --------------------------------------------------------------------------------------------------
  Clock name        Clock freq        Clock capabilities
  ----------------- ----------------- --------------------------------------------------------------
  APB_CLK           80 MHz            /

  RC_FAST_CLK       \~ 20 MHz         Dynamic Frequency Scaling compatible, Light-sleep compatible

  XTAL_CLK          40 MHz            Dynamic Frequency Scaling compatible
  --------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::: only
esp32c2

  --------------------------------------------------------------------------------------------------
  Clock name        Clock freq        Clock capabilities
  ----------------- ----------------- --------------------------------------------------------------
  PLL_60M_CLK       60 MHz            /

  RC_FAST_CLK       \~ 20 MHz         Dynamic Frequency Scaling compatible, Light-sleep compatible

  XTAL_CLK          40/26 MHz         Dynamic Frequency Scaling compatible
  --------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::: only
esp32c5

  --------------------------------------------------------------------------------------------------
  Clock name        Clock freq        Clock capabilities
  ----------------- ----------------- --------------------------------------------------------------
  PLL_80M_CLK       80 MHz            /

  RC_FAST_CLK       \~ 17.5 MHz       Dynamic Frequency Scaling compatible, Light-sleep compatible

  XTAL_CLK          48 MHz            Dynamic Frequency Scaling compatible
  --------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::: only
esp32c6 or esp32c61 or esp32p4

  --------------------------------------------------------------------------------------------------
  Clock name        Clock freq        Clock capabilities
  ----------------- ----------------- --------------------------------------------------------------
  PLL_80M_CLK       80 MHz            /

  RC_FAST_CLK       \~ 17.5 MHz       Dynamic Frequency Scaling compatible, Light-sleep compatible

  XTAL_CLK          40 MHz            Dynamic Frequency Scaling compatible
  --------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::: only
esp32h2

  --------------------------------------------------------------------------------------------------
  Clock name        Clock freq        Clock capabilities
  ----------------- ----------------- --------------------------------------------------------------
  PLL_96M_CLK       96 MHz            /

  RC_FAST_CLK       \~ 8 MHz          Dynamic Frequency Scaling compatible, Light-sleep compatible

  XTAL_CLK          32 MHz            Dynamic Frequency Scaling compatible
  --------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::: only
esp32h21 or esp32h4

  --------------------------------------------------------------------------------------------------
  Clock name        Clock freq        Clock capabilities
  ----------------- ----------------- --------------------------------------------------------------
  PLL_96M_CLK       96 MHz            /

  RC_FAST_CLK       \~ 20 MHz         Dynamic Frequency Scaling compatible, Light-sleep compatible

  XTAL_CLK          32 MHz            Dynamic Frequency Scaling compatible
  --------------------------------------------------------------------------------------------------

  : Characteristics of {IDF_TARGET_NAME} LEDC source clocks
:::

::::::: note
::: title
Note
:::

::: only
SOC_CLK_RC_FAST_SUPPORT_CALIBRATION

1.  On {IDF_TARGET_NAME}, if RC_FAST_CLK is chosen as the LEDC clock source, an internal calibration will be performed to get the exact frequency of the clock. This ensures the accuracy of output PWM signal frequency.
:::

::: only
not SOC_CLK_RC_FAST_SUPPORT_CALIBRATION

1.  On {IDF_TARGET_NAME}, if RC_FAST_CLK is chosen as the LEDC clock source, you may see the frequency of output PWM signal is not very accurate. This is because no internal calibration is performed to get the exact frequency of the clock due to hardware limitation, a theoretic frequency value is used.
:::

::: only
not SOC_LEDC_HAS_TIMER_SPECIFIC_MUX

2.  For {IDF_TARGET_NAME}, all timers share one clock source. In other words, it is impossible to use different clock sources for different timers.
:::
:::::::

The LEDC driver offers a helper function `ledc_find_suitable_duty_resolution`{.interpreted-text role="cpp:func"} to find the maximum possible resolution for the timer, given the source clock frequency and the desired PWM signal frequency.

When a timer is no longer needed by any channel, it can be deconfigured by calling the same function `ledc_timer_config`{.interpreted-text role="cpp:func"}. The configuration structure `ledc_timer_config_t`{.interpreted-text role="cpp:type"} passes in should be:

- `ledc_timer_config_t::speed_mode`{.interpreted-text role="cpp:member"} The speed mode of the timer which wants to be deconfigured belongs to (`ledc_mode_t`{.interpreted-text role="cpp:type"})
- `ledc_timer_config_t::timer_num`{.interpreted-text role="cpp:member"} The ID of the timers which wants to be deconfigured (`ledc_timer_t`{.interpreted-text role="cpp:type"})
- `ledc_timer_config_t::deconfigure`{.interpreted-text role="cpp:member"} Set this to true so that the timer specified can be deconfigured

### Channel Configuration {#ledc-api-configure-channel}

When the timer is set up, configure the desired channel (one out of `ledc_channel_t`{.interpreted-text role="cpp:type"}). This is done by calling the function `ledc_channel_config`{.interpreted-text role="cpp:func"}.

Similar to the timer configuration, the channel setup function should be passed a structure `ledc_channel_config_t`{.interpreted-text role="cpp:type"} that contains the channel\'s configuration parameters.

At this point, the channel should start operating and generating the PWM signal on the selected GPIO, as configured in `ledc_channel_config_t`{.interpreted-text role="cpp:type"}, with the frequency specified in the timer settings and the given duty cycle. The channel operation (signal generation) can be suspended at any time by calling the function `ledc_stop`{.interpreted-text role="cpp:func"}.

### Change PWM Signal {#ledc-api-change-pwm-signal}

Once the channel starts operating and generating the PWM signal with the constant duty cycle and frequency, there are a couple of ways to change this signal. When driving LEDs, primarily the duty cycle is changed to vary the light intensity.

The following two sections describe how to change the duty cycle using software and hardware fading. If required, the signal\'s frequency can also be changed; it is covered in Section `ledc-api-change-pwm-frequency`{.interpreted-text role="ref"}.

::::: only
not esp32

:::: note
::: title
Note
:::

All the timers and channels in the {IDF_TARGET_NAME}\'s LED PWM Controller only support low speed mode. Any change of PWM settings must be explicitly triggered by software (see below).
::::
:::::

#### Change PWM Duty Cycle Using Software

To set the duty cycle, use the dedicated function `ledc_set_duty`{.interpreted-text role="cpp:func"}. After that, call `ledc_update_duty`{.interpreted-text role="cpp:func"} to activate the changes. To check the currently set value, use the corresponding `_get_` function `ledc_get_duty`{.interpreted-text role="cpp:func"}.

Another way to set the duty cycle, as well as some other channel parameters, is by calling `ledc_channel_config`{.interpreted-text role="cpp:func"} covered in Section `ledc-api-configure-channel`{.interpreted-text role="ref"}.

The range of the duty cycle values passed to functions depends on selected `duty_resolution` and should be from `0` to `(2 ** duty_resolution)`. For example, if the selected duty resolution is 10, then the duty cycle values can range from 0 to 1024. This provides the resolution of \~ 0.1%.

::::::: only
esp32 or esp32s2 or esp32s3 or esp32c3 or esp32c2 or esp32c6 or esp32h2 or esp32p4

:::: warning
::: title
Warning
:::

On {IDF_TARGET_NAME}, when channel\'s binded timer selects its maximum duty resolution, the duty cycle value cannot be set to `(2 ** duty_resolution)`. Otherwise, the internal duty counter in the hardware will overflow and be messed up.
::::

::: only
esp32h2

The hardware limitation above only applies to chip revision before v1.2.
:::

::: only
esp32p4

The hardware limitation above only applies to chip revision before v3.0.
:::
:::::::

#### Change PWM Duty Cycle Using Hardware

The LEDC hardware provides the means to gradually transition from one duty cycle value to another. To use this functionality, enable fading with `ledc_fade_func_install`{.interpreted-text role="cpp:func"} and then configure it by calling one of the available fading functions:

- `ledc_set_fade_with_time`{.interpreted-text role="cpp:func"}
- `ledc_set_fade_with_step`{.interpreted-text role="cpp:func"}
- `ledc_set_fade`{.interpreted-text role="cpp:func"}

::: only
SOC_LEDC_GAMMA_CURVE_FADE_SUPPORTED

On {IDF_TARGET_NAME}, the hardware additionally allows to perform up to {IDF_TARGET_LEDC_MAX_FADE_RANGE_NUM} consecutive linear fades without CPU intervention. This feature can be useful if you want to do a fade with gamma correction.

The luminance perceived by human eyes does not have a linear relationship with the PWM duty cycle. In order to make human feel the LED is dimming or lighting linearly, the change in duty cycle should be non-linear, which is the so-called gamma correction. The LED controller can simulate a gamma curve fading by piecewise linear approximation. `ledc_fill_multi_fade_param_list`{.interpreted-text role="cpp:func"} is a function that can help to construct the parameters for the piecewise linear fades. First, you need to allocate a memory block for saving the fade parameters, then by providing start/end PWM duty cycle values, gamma correction function, and the total number of desired linear segments to the helper function, it will fill the calculation results into the allocated space. You can also construct the array of `ledc_fade_param_config_t`{.interpreted-text role="cpp:type"} manually. Once the fade parameter structs are prepared, a consecutive fading can be configured by passing the pointer to the prepared `ledc_fade_param_config_t`{.interpreted-text role="cpp:type"} list and the total number of fade ranges to `ledc_set_multi_fade`{.interpreted-text role="cpp:func"}.
:::

::: only
esp32

Start fading with `ledc_fade_start`{.interpreted-text role="cpp:func"}. A fade can be operated in blocking or non-blocking mode, please check `ledc_fade_mode_t`{.interpreted-text role="cpp:enum"} for the difference between the two available fade modes. Note that with either fade mode, the next fade or fixed-duty update will not take effect until the last fade finishes. Due to hardware limitations, there is no way to stop a fade before it reaches its target duty.
:::

::: only
not esp32

Start fading with `ledc_fade_start`{.interpreted-text role="cpp:func"}. A fade can be operated in blocking or non-blocking mode, please check `ledc_fade_mode_t`{.interpreted-text role="cpp:enum"} for the difference between the two available fade modes. Note that with either fade mode, the next fade or fixed-duty update will not take effect until the last fade finishes or is stopped. `ledc_fade_stop`{.interpreted-text role="cpp:func"} has to be called to stop a fade that is in progress.
:::

To get a notification about the completion of a fade operation, a fade end callback function can be registered for each channel by calling `ledc_cb_register`{.interpreted-text role="cpp:func"} after the fade service being installed. The fade end callback prototype is defined in `ledc_cb_t`{.interpreted-text role="cpp:type"}, where you should return a boolean value from the callback function, indicating whether a high priority task is woken up by this callback function. It is worth mentioning, the callback and the function invoked by itself should be placed in IRAM, as the interrupt service routine is in IRAM. `ledc_cb_register`{.interpreted-text role="cpp:func"} will print a warning message if it finds the addresses of callback and user context are incorrect.

If not required anymore, fading and an associated interrupt can be disabled with `ledc_fade_func_uninstall`{.interpreted-text role="cpp:func"}.

#### Change PWM Frequency {#ledc-api-change-pwm-frequency}

The LEDC API provides several ways to change the PWM frequency \"on the fly\":

> - Set the frequency by calling `ledc_set_freq`{.interpreted-text role="cpp:func"}. There is a corresponding function `ledc_get_freq`{.interpreted-text role="cpp:func"} to check the current frequency.
> - Change the frequency and the duty resolution by calling `ledc_bind_channel_timer`{.interpreted-text role="cpp:func"} to bind some other timer to the channel.
> - Change the channel\'s timer by calling `ledc_channel_config`{.interpreted-text role="cpp:func"}.

#### More Control Over PWM

There are several individual timer-specific functions that can be used to change PWM output:

- `ledc_timer_rst`{.interpreted-text role="cpp:func"}
- `ledc_timer_pause`{.interpreted-text role="cpp:func"}
- `ledc_timer_resume`{.interpreted-text role="cpp:func"}

The first function is called \"behind the scenes\" by `ledc_timer_config`{.interpreted-text role="cpp:func"} to provide a startup of a timer after it is configured.

::: only
SOC_LEDC_SUPPORT_ETM and SOC_ETM_SUPPORTED

## LEDC\'s ETM Events and Tasks

LEDC can generate various events that can be connected to the `ETM </api-reference/peripherals/etm>`{.interpreted-text role="doc"} module. Timer\'s supported events are listed in `ledc_timer_etm_event_type_t`{.interpreted-text role="cpp:type"}, and channel\'s supported events are listed in `ledc_channel_etm_event_type_t`{.interpreted-text role="cpp:type"}. Users can create an `ETM event` handle by calling `ledc_timer_new_etm_event`{.interpreted-text role="cpp:func"} or `ledc_channel_new_etm_event`{.interpreted-text role="cpp:func"} respectively. LEDC also supports some tasks that can be triggered by other events and executed automatically. Timer\'s supported tasks are listed in `ledc_timer_etm_task_type_t`{.interpreted-text role="cpp:type"}, and channel\'s supported tasks are listed in `ledc_channel_etm_task_type_t`{.interpreted-text role="cpp:type"}. Users can create an `ETM task` handle by calling `ledc_timer_new_etm_task`{.interpreted-text role="cpp:func"} or `ledc_channel_new_etm_task`{.interpreted-text role="cpp:func"} respectively.

Some useful applications of ETM with LEDC are:

> - To generate a PWM signal with certain number of pulses
> - To synchronize the PWM period with an external signal
> - To start / stop the PWM signal output or a fading without CPU intervention

For how to connect the LEDC events and tasks to the ETM channel, please refer to the `ETM </api-reference/peripherals/etm>`{.interpreted-text role="doc"} documentation.
:::

## Power Management

LEDC driver does not utilize power management lock to prevent the system from going into Light-sleep. Instead, the LEDC peripheral power domain state and the PWM signal output behavior during sleep can be chosen by configuring `ledc_channel_config_t::sleep_mode`{.interpreted-text role="cpp:member"}. The default mode is `LEDC_SLEEP_MODE_NO_ALIVE_NO_PD`{.interpreted-text role="cpp:enumerator"}, which stands for no signal output and LEDC power domain will not be powered down during sleep.

If signal output needs to be maintained in Light-sleep, then select `LEDC_SLEEP_MODE_KEEP_ALIVE`{.interpreted-text role="cpp:enumerator"}. As long as the binded LEDC timer clock source is Light-sleep compatible, the PWM signal can continue its output even the system enters Light-sleep. The cost is a higher power consumption in sleep, since the clock source and the power domain where LEDC belongs to cannot be powered down. Note that, if there is an unfinished fade before entering sleep, the fade can also continue during sleep, but the target duty might not be reached exactly. It will adjust to the target duty after wake-up.

::: only
SOC_LEDC_SUPPORT_SLEEP_RETENTION

There is another sleep mode, `LEDC_SLEEP_MODE_NO_ALIVE_ALLOW_PD`{.interpreted-text role="cpp:enumerator"}, can save some power consumption in sleep, but at the expense of more memory being consumed. The system retains LEDC register context before entering Light-sleep and restores them after waking up, so that the LEDC power domain can be powered down during sleep. Any unfinished fade will not resume upon waking up from sleep, instead, it will output a PWM signal with a fixed duty cycle that matches the duty cycle just before entering sleep.
:::

::: only
esp32

## LEDC High and Low Speed Mode {#ledc-api-high_low_speed_mode}

High speed mode enables a glitch-free changeover of timer settings. This means that if the timer settings are modified, the changes will be applied automatically on the next overflow interrupt of the timer. In contrast, when updating the low-speed timer, the change of settings should be explicitly triggered by software. The LEDC driver handles it in the background, e.g., when `ledc_timer_config`{.interpreted-text role="cpp:func"} is called.

For additional details regarding speed modes, see **{IDF_TARGET_NAME} Technical Reference Manual** \> **LED PWM Controller (LEDC)** \[[PDF]({IDF_TARGET_TRM_EN_URL}#ledpwm)\].
:::

::: only
not esp32
:::

## Supported Range of Frequency and Duty Resolutions

The LED PWM Controller is designed primarily to drive LEDs. It provides a large flexibility of PWM duty cycle settings. For instance, the PWM frequency of 5 kHz can have the maximum duty resolution of 13 bits. This means that the duty can be set anywhere from 0 to 100% with a resolution of \~ 0.012% (2 \*\* 13 = 8192 discrete levels of the LED intensity). Note, however, that these parameters depend on the clock signal clocking the LED PWM Controller timer which in turn clocks the channel (see `timer configuration <ledc-api-configure-timer>`{.interpreted-text role="ref"} and the **{IDF_TARGET_NAME} Technical Reference Manual** \> **LED PWM Controller (LEDC)** \[[PDF]({IDF_TARGET_TRM_EN_URL}#ledpwm)\]).

The LEDC can be used for generating signals at much higher frequencies that are sufficient enough to clock other devices, e.g., a digital camera module. In this case, the maximum available frequency is 40 MHz with duty resolution of 1 bit. This means that the duty cycle is fixed at 50% and cannot be adjusted.

The LEDC API is designed to report an error when trying to set a frequency and a duty resolution that exceed the range of LEDC\'s hardware. For example, an attempt to set the frequency to 20 MHz and the duty resolution to 3 bits results in the following error reported on a serial monitor:

``` none
E (196) ledc: requested frequency and duty resolution cannot be achieved, try reducing freq_hz or duty_resolution. div_param=128
```

In such a situation, either the duty resolution or the frequency must be reduced. For example, setting the duty resolution to 2 resolves this issue and makes it possible to set the duty cycle at 25% steps, i.e., at 25%, 50% or 75%.

The LEDC driver also captures and reports attempts to configure frequency/duty resolution combinations that are below the supported minimum, e.g.,:

``` none
E (196) ledc: requested frequency and duty resolution cannot be achieved, try increasing freq_hz or duty_resolution. div_param=128000000
```

The duty resolution is normally set using `ledc_timer_bit_t`{.interpreted-text role="cpp:type"}. This enumeration covers the range from 10 to 15 bits. If a smaller duty resolution is required (from 10 down to 1), enter the equivalent numeric values directly.

## Application Example

::: list
- `peripherals/ledc/ledc_basic`{.interpreted-text role="example"} demonstrates how to use the LEDC to generate a PWM signal in LOW SPEED mode.

\* `peripherals/ledc/ledc_fade`{.interpreted-text role="example"} demonstrates how to control the intensity of LEDs using the LEDC fade functionality. :SOC_LEDC_GAMMA_CURVE_FADE_SUPPORTED: \* `peripherals/ledc/ledc_gamma_curve_fade`{.interpreted-text role="example"} demonstrates how to use the LEDC for color control of RGB LEDs with gamma correction. :SOC_LEDC_SUPPORT_ETM and SOC_ETM_SUPPORTED: \* `peripherals/ledc/ledc_dimmer`{.interpreted-text role="example"} demonstrates how to use the LEDC and ETM to generate TRIAC gate trigger pulses that are synchronized to the mains zero‑cross.
:::

## API Reference

::: include-build-file
inc/ledc.inc
:::

::: include-build-file
inc/ledc_types.inc
:::

:::: only
SOC_LEDC_SUPPORT_ETM and SOC_ETM_SUPPORTED

::: include-build-file
inc/ledc_etm.inc
:::
::::
