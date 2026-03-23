

```markdown
Figure 8.3-1. Clock Configuration Example

Figure 8.3-1 shows the clock structure of I2C. The clock structure of other peripherals is similar to this one.
CLK_SWITCH is used to select a clock output and CLK_GATE to turn on/off the clock.

In scenarios that require low power consumption, when the peripheral is not in use, in addition to turning off
the function clock, the bus clock of the peripheral can also be turned off to further lower power consumption.

Note that if you turn off the bus clock first, the function clock may continue working. It is recommended to
turn off the function clock first and then the bus clock when turning off the clocks. It is also recommended to
turn on the bus clock first and then the function clock when turning on the clocks.

8.4 Register Summary

8.4.1 PCR Registers

The addresses in this section are relative to the Power/Clock/Reset (PCR) Register base address provided in
Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```