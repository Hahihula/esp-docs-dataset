

```markdown
## 8.5.4.2 LP GPIO Matrix

For outputs, LP GPIO matrix only supports the Simple GPIO Output function. For the detailed programming, please refer to Section 8.5.2.

## 8.6 Direct Input and Output via IO MUX

### 8.6.1 Overview

Some digital signals such as SPI and JTAG can bypass GPIO matrix for better high-frequency digital performance. In this case, IO MUX is used to connect these pins directly to peripherals. This option is less flexible than routing signals via GPIO matrix, as the IO MUX register for each GPIO pin can only select from a limited number of functions, but high-frequency digital performance can be improved.

ESP32-C5 provides 7 GPIO pins (GPIO0~GPIO6) with low power (LP) capabilities. These pins can be controlled by either HP IO MUX or LP IO MUX. If controlled by LP IO MUX, these pins will bypass HP IO MUX and HP GPIO matrix for the use by peripherals in LP system.

When configured as LP GPIOs, the pins can still be controlled by the peripherals in LP system during chip Deep-sleep, and wake up the chip from Deep-sleep.

### 8.6.2 Functional Description

The pins with LP functions (GPIO0~GPIO6) are controlled by bit[n] of LP_AON_GPIO_MUX_SEL in LP_AON_GPIO_MUX_REG (n = 0~6). By default, all these bits are set to 0, routing all input/output signals via HP IO MUX.

If bit[n] is set to 1 in LP_AON_GPIO_MUX_SEL, then input/output signals are controlled by LP IO MUX. In this mode, LP_IO_MUX_GPIO_n_REG is used to control the LP GPIO pins. See 8.14-1 for the LP functions of each LP GPIO pin. Note that LP_IO_MUX_GPIO_n_REG applies the LP GPIO pin numbering. In ESP32-C5, the numbering of LP GPIO pins is the same as that of the HP GPIO pins.

#### 8.6.2.1 HP IO MUX

Two fields must be configured in order to bypass HP GPIO matrix for HP peripheral input signals:

1. `IO_MUX_GPIO_n_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Table 8.13-1.
2. Clear `GPIO_SIGn_IN_SEL` to route the input directly to the peripheral.

To bypass HP GPIO matrix for HP peripheral output signals, `IO_MUX_GPIO_n_MCU_SEL` for the GPIO pin must be set to the required pin function.

#### 8.6.2.2 LP IO MUX

To bypass LP GPIO matrix for LP peripheral input/output signals, `LP_IO_MUX_GPIO_n_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Table 8.14-1.
```