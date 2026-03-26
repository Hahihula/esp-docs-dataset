

```markdown
## 9.6.2.2 LP IO MUX

Two fields must be configured in order to bypass LP GPIO matrix for LP peripheral input signals:

1. `LP_IOMUX_PADn_MUX_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Table 9.15-1.
2. Clear `LP_GPIO_GPIO_Sign_IN_SEL` to route the input directly to the peripheral.

To bypass LP GPIO matrix for LP peripheral output signals, `LP_IOMUX_PADn_MUX_SEL` for the GPIO pin must be set to the required pin function.

**Note:**
Not all signals can be directly connected to peripheral via IO MUX. Some input/output signals can only be connected to peripheral via GPIO matrix.
```

```markdown
## 9.7 Analog Functions

### 9.7.1 Overview

ESP32-P4 provides 34 GPIO pins with analog functions, including 16 LP GPIO pins and 18 HP GPIO pins. See Table 9.16-1.

### 9.7.2 Analog Functions

When the pin is used for analog purpose, make sure this pin is left floating by configuring registers. By such way, the external analog signal is directly connected to internal analog signal via GPIO pin. The configuration is as follows:

* Clear `IO_MUX_GPIOFn_FUNC_IE`, `IO_MUX_GPIOFn_FUN_WPU`, and `IO_MUX_GPIOFn_FUN_WPD`, to set the pin floating.
* Write 1 to the corresponding bit in `GPIO_ENABLE_W1TC` and `GPIO_ENABLE1_W1TC`, to clear output enable.

To use these functions listed in Table 9.16-1, please refer to the following related chapters:

* For XTAL_32K related functions, see Chapter 14 Low-Power Management.
* For TOUCH related functions, see Chapter 60 Touch Sensor (TOUCH).
* For ADC related functions, see Chapter 62 ADC Controller (ADC).
* For COMP related functions, see Chapter 63 Analog Voltage Comparator.

**Note:**
GPIO51 ~ GPIO54 each has two different analog functions, which can be used simultaneously.
```