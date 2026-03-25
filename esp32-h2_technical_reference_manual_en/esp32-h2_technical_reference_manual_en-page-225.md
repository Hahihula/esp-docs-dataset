

```markdown
## 6.5.4.2 SDM Configuration

The configuration of SDM is shown below:

- Route one of SDM outputs to a pin via GPIO matrix, see Section 6.5.2.
- Enable the modulator clock by setting `GPIO_EXT_FUNCTION_CLK_EN`.
- Configure the divider value by setting `GPIO_EXT_SDn_PRESCALE`.
- Configure the duty cycle of SDM output signal by setting `GPIO_EXT_SDn_IN`.

## 6.6 Direct Input and Output via IO MUX

### 6.6.1 Overview

Some digital signals (SPI and JTAG) can bypass GPIO matrix for better high-frequency digital performance. In this case, IO MUX is used to connect these pins directly to peripherals.

This option is less flexible than routing signals via GPIO matrix, as the IO MUX register for each GPIO pin can only select from a limited number of functions, but high-frequency digital performance can be improved.

### 6.6.2 Functional Description

Two fields must be configured in order to bypass GPIO matrix for peripheral input signals:

1. `IO_MUX_GPIO[n]_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Section 6.13.
2. Clear `GPIO_SIGn_IN_SEL` to route the input directly to the peripheral.

To bypass GPIO matrix for peripheral output signals, `IO_MUX_GPIO[n]_MCU_SEL` for the GPIO pin must be set to the required pin function.

**Note:**
Not all signals can be directly connected to peripheral via IO MUX. Some input/output signals can only be connected to the peripheral via GPIO matrix.

## 6.7 Analog Functions of GPIO Pins

Some GPIO pins in ESP32-H2 provide analog functions. When the pin is used for analog purposes, make sure that pull-up and pull-down resistors are disabled by the following configuration:

- Set `IO_MUX_GPIO[n]_MCU_SEL` to 1, and clear `IO_MUX_GPIO[n]_FUN_IE`, `IO_MUX_GPIO[n]_FUN_WPU`, `IO_MUX_GPIO[n]_FUN_WPD`.
- Write 1 to `GPIO_ENABLE_W1TC[n]`, to clear output enable.

See Table 6.14-1 for analog functions of ESP32-H2 pins.
```