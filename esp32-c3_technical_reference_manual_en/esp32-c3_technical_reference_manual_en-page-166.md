

```markdown
5.5.4.2 SDM Configuration

The configuration of SDM is shown below:

* Route one of SDM outputs to a pin via GPIO matrix, see Section 5.5.2.
* Enable the modulator clock by setting the register `GPIOISD_FUNCTION_CLK_EN`.
* Configure the divider value by setting the register `GPIOISD_SDn_PRESCALE`.
* Configure the duty cycle of SDM output signal by setting the register `GPIOISD_SDn_IN`.

5.6 Direct Input and Output via IO MUX

5.6.1 Overview

Some high-speed signals (SPI and JTAG) can bypass GPIO matrix for better high-frequency digital performance. In this case, IO MUX is used to connect these pins directly to peripherals.

This option is less flexible than routing signals via GPIO matrix, as the IO MUX register for each GPIO pin can only select from a limited number of functions, but high-frequency digital performance can be improved.

5.6.2 Functional Description

Two registers must be configured in order to bypass GPIO matrix for peripheral input signals:

1. `IO_MUX_GPIO[n]_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Section 5.12.
2. Clear `GPIO_SIGn_IN_SEL` to route the input directly to the peripheral.

To bypass GPIO matrix for peripheral output signals, `IO_MUX_GPIO[n]_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Section 5.12.

Note:
Not all signals can be directly connected to peripheral via IO MUX. Some input/output signals can only be connected to peripheral via GPIO matrix.

5.7 Analog Functions of GPIO Pins

Some GPIO pins in ESP32-C3 provide analog functions. When the pin is used for analog purpose, make sure that pull-up and pull-down resistors are disabled by following configuration:

* Set `IO_MUX_GPIO[n]_MCU_SEL` to 1, and clear `IO_MUX_GPIO[n]_FUN_IE`, `IO_MUX_GPIO[n]_FUN_WPU`, `IO_MUX_GPIO[n]_FUN_WPD`.
* Write 1 to `GPIO_ENABLE_W1TC[n]`, to clear output enable.

See Table 5.13-1 for analog functions of ESP32-C3 pins.
```