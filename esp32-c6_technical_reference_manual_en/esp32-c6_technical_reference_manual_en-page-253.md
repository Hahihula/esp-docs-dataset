

```markdown
## 7.6.2 Functional Description

Two fields must be configured in order to bypass GPIO matrix for peripheral input signals:

1. `IO_MUX_GPIO[n]_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Section 7.12.
2. Clear `GPIO_SIGn_IN_SEL` to route the input directly to the peripheral.

To bypass GPIO matrix for peripheral output signals, `IO_MUX_GPIO[n]_MCU_SEL` for the GPIO pin must be set to the required pin function.

**Note:**
Not all signals can be directly connected to peripheral via IO MUX. Some input/output signals can only be connected to peripheral via GPIO matrix.
```

```markdown
## 7.7 LP IO MUX for Low Power and Analog Input/Output

### 7.7.1 Overview

ESP32-C6 provides eight GPIO pins with low power (LP) capabilities and analog functions. These pins can be controlled by either IO MUX or LP IO MUX.

If controlled by LP IO MUX, these pins will bypass IO MUX and GPIO matrix for the use by ULP and peripherals in LP system.

When configured as LP GPIOs, the pins can still be controlled by ULP or the peripherals in LP system during chip Deep-sleep, and wake up the chip from Deep-sleep.

### 7.7.2 Low Power Capabilities

The pins with LP functions are controlled by `LP_AON_GPIO_MUX_SEL[n]` (`n = GPIO0 ~ GPIO7`) bit in register `LP_AON_GPIO_MUX_REG`. By default, all bits in these registers are set to 0, routing all input/output signals via IO MUX.

If `LP_AON_GPIO_MUX_SEL[n]` is set to 1, then input/output signals are controlled by LP IO MUX. In this mode, `LP_IO_GPIO[n]_REG` is used to control the LP GPIO pins. See [7.13-1](#) for the LP functions of each LP GPIO pin.

Note that `LP_IO_GPIO[n]_REG` applies the LP GPIO pin numbering, not the GPIO pin numbering.

### 7.7.3 Analog Functions

When the pin is used for analog purpose, make sure this pin is left floating by configuring `LP_IO_GPIO[n]_REG`. By such way, the external analog signal is directly connected to internal analog signal via GPIO pin. The configuration is as follows:

- Set `LP_AON_GPIO_MUX_SEL[n]`, to select LP IO MUX to route input and output signals.
- Clear `LP_GPIO_GPIO[n]_FUN_IE`, `LP_GPIO_GPIO[n]_FUN_RUE`, and `LP_GPIO_GPIO[n]_FUN_RDE`, to set the pin floating.
- Configure `LP_GPIO_GPIO[n]_FUN_SEL` to 0, i.e., select Analog Function 0;
```