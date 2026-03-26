

```markdown
Note:
* The output signal from a single peripheral can be sent to multiple pins simultaneously.
* The output signal can be inverted by setting `GPIO_FUNCx_OUT_INV_SEL`.

9.5.4.2 LP GPIO Matrix

The programming procedure for peripheral input via the LP GPIO matrix resembles that of 9.5.4.1. However, it's worth noting that the control and status registers must use LP GPIO matrix registers. See Section 9.19.4 and Section 9.19.5.

9.6 Direct Input and Output via IO MUX

9.6.1 Overview

Some digital signals (SDMMC, EMAC, etc.) can bypass GPIO matrix for better high-frequency digital performance. In this case, IO MUX is used to connect these pins directly to peripherals. This option is less flexible than routing signals via GPIO matrix, as the IO MUX register for each GPIO pin can only select from a limited number of functions, but high-frequency digital performance can be improved.

ESP32-P4 provides 16 GPIO pins with low power (LP) capabilities. These pins can be controlled by either HP IO MUX or LP IO MUX. If controlled by LP IO MUX, these pins will bypass HP IO MUX and HP GPIO matrix for the use by peripherals in LP system.

When configured as LP GPIOs, the pins can still be controlled by the peripherals in LP system during chip Deep-sleep, and wake up the chip from Deep-sleep.

9.6.2 Functional Description

The pins with LP functions (GPIO0 ~ GPIO15) are controlled by `LP_IOMUX_PADn_MUX_SEL` (`n: 0 ~ 15`) in register `LP_IOMUX_PADn_REG`. By default, all bits in these registers are set to 0, routing all input/output signals via HP IO MUX.

If `LP_IOMUX_PADn_MUX_SEL` is set, then input/output signals are controlled by LP IO MUX. In this mode, `LP_IOMUX_PADn_REG` is used to control the LP GPIO pins. See 9.15-1 for the LP functions of each LP GPIO pin. Note that `LP_IOMUX_PADn_REG` applies the LP GPIO pin numbering, not the HP GPIO pin numbering.

9.6.2.1 HP IO MUX

Two fields must be configured in order to bypass HP GPIO matrix for HP peripheral input signals:

1. `IO_MUX_GPIOon_MCU_SEL` for the GPIO pin must be set to the required pin function. For the list of pin functions, please refer to Table 9.14-1.

2. Clear `GPIO_SIGn_IN_SEL` to route the input directly to the peripheral.

To bypass HP GPIO matrix for HP peripheral output signals, `IO_MUX_GPIOon_MCU_SEL` for the GPIO pin must be set to the required pin function.
```