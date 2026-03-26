

```markdown
Figure 10.3-1. Clock Configuration Example

Note:
In this chapter, all divisor configuration registers are configured with the actual divisor minus 1.
```

Figure 10.3-1 shows the clock structure of I2C. The clock structure of other peripherals is similar to this one. CLK_SWITCH is used to select a clock output and CLK_GATE to turn on/off the clock.

In scenarios that require low power consumption, when the peripheral is not in use, in addition to turning off the function clock, the bus clock of the peripheral can also be turned off to further lower power consumption.

Note that if you turn off the bus clock first, the functional clock may continue working. Therefore, when turning off clocks, it is recommended to turn off the functional clock first and then the bus clock; when turning on clocks, it is recommended to turn on the bus clock first and then the functional clock.
```