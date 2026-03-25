

Chapter 7 Reset and Clock

The functional clock of most peripherals can be selected from multiple clock sources. For clock gating registers, whether they are used to gate the bus clock (AHB_CLK, APB_CLK) or the functional clock will be stated in the corresponding register descriptions.

Bus clock switches, functional clock switches, and configuration registers for clock source selection and clock frequency division are grouped into the PCR module. For more information, see Section 7.4 Register Summary.

When a peripheral is not working, users can turn off its functional clock by configuring related PCR registers. Turning off the peripheral's functional clock does not affect the rest of the system.

Take the I2C clock configuration as an example.

Figure 7.3-1 shows the clock structure of I2C. The clock structure of other peripherals is similar to this one. CLK_SWITCH is used to select a clock output and CLK_GATE to turn on/off the clock.

In scenarios that require low power consumption, when the peripheral is not in use, in addition to turning off the functional clock, the bus clock of the peripheral can also be turned off to further lower the power consumption.

Note that if you turn off the bus clock first, the functional clock may continue working. Therefore, when turning off clocks, it is recommended to turn off the functional clock first and then the bus clock; when turning on clocks, it is recommended to turn on the bus clock first and then the functional clock.

Note:
In this chapter, all divisor configuration registers are configured with the actual divisor minus 1.

Figure 7.3-1. Clock Configuration Example

POWER & CLOCK MODULE
APB_CLK → CLK_GATE → I2C_APB_CLK
PCR_REG
RC_FAST_CLK & XTAL_CLK → CLK_SWITCH & CLK_GATE & CLK_DIV → I2C_SCLK → I2C

GoBack

Espressif Systems
280
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback