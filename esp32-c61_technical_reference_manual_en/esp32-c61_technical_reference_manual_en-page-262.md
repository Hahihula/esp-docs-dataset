

```markdown
## 6.5.3.2 LP GPIO Matrix

For outputs, LP GPIO matrix only supports the Simple GPIO Output function. For the detailed programming, please refer to Section 6.5.2.

## 6.6 Direct Input and Output via IO MUX

### 6.6.1 Overview

To achieve better high-frequency performance, digital signals such as SPI and JTAG can bypass the GPIO matrix and be routed directly to peripherals through the IO MUX. While this method is less flexible than using the GPIO matrix as each GPIO pin’s IO MUX register offers only a limited set of functions, it significantly improves signal integrity for high-speed interfaces.

ESP32-C61 provides 7 GPIO pins (GPIO0~GPIO6) with low power (LP) capabilities. These pins can be controlled by either HP IO MUX or LP IO MUX. If controlled by LP IO MUX, these pins will bypass HP IO MUX and HP GPIO matrix for the use by peripherals in LP system.

When configured as LP GPIOs, these pins remain operational and can be controlled by LP system peripherals even during Deep-sleep mode. They can also be used to wake the chip from Deep-sleep.

### 6.6.2 Functional Description

The pins with LP functions (GPIO0~GPIO6) are controlled by bit[n] of LP_AON_GPIO_MUX_SEL in LP_AON_GPIO_MUX_REG (n = 0~6). By default, all these bits are set to 0, routing all input/output signals via HP IO MUX.

If bit[n] is set to 1 in LP_AON_GPIO_MUX_SEL, then input/output signals are controlled by LP IO MUX. In this mode, LP_IO_MUX_GPIOn_REG is used to control the LP GPIO pins. See 6.14-1 for the LP functions of each LP GPIO pin. Note that LP_IO_MUX_GPIOn_REG applies the LP GPIO pin numbering. In ESP32-C61, the numbering of LP GPIO pins is the same as that of the HP GPIO pins.

#### 6.6.2.1 HP IO MUX

Two fields must be configured in order to bypass HP GPIO matrix for HP peripheral input signals:

1. `IO_MUX_GPIOn_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Table 6.13-1.
2. Clear `GPIO_SIgn_IN_SEL` to route the input directly to the peripheral.

To bypass HP GPIO matrix for HP peripheral output signals, `IO_MUX_GPIOn_MCU_SEL` for the GPIO pin must be set to the required pin function.

**Note:**
Not all signals can be directly connected to peripheral via HP IO MUX. Some input/output signals can only be connected to peripheral via HP GPIO matrix. See Table 6.12-1.
```