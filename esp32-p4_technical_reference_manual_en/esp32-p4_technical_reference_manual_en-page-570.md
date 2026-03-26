

```markdown
lowest priority.

- When GPIOy is controlled by ETM task channel, the values of GPIO_OUT_REG, GPIO_FUNCn_OUT_INV_SEL, and GPIO_FUNCn_OUT_SEL may be modified by the hardware. For such reason, it's recommended to reconfigure these registers when the GPIO is free from the control of ETM task channel.

GPIO has eight event channels, and the ETM events that each event channel can generate are:

- GPIO_EVT_CHx_RISE_EDGE: Indicates that the output signal of the corresponding GPIO Filter (see Figure 9.3-1) has a rising edge.
- GPIO_EVT_CHx_FALL_EDGE: Indicates that the output signal of the corresponding GPIO Filter (see Figure 9.3-1) has a falling edge.
- GPIO_EVT_CHx_ANY_EDGE: Indicates that the output signal of the corresponding GPIO Filter (see Figure 9.3-1) is reversed.

The specific configuration of the event channel is as follows:

- Set GPIO_EXT_ETM_CHx_EVENT_EN to enable event channel x (0 ~ 7).
- Configure GPIO_EXT_ETM_CHx_EVENT_SEL to y (0 ~ 54), i.e., select one from the 55 GPIOs.

Note:
One GPIO can be selected by one or more event channels.
```

## 9.18 Interrupts

ESP32-P4's HP IO MUX and HP GPIO matrix can generate the following interrupt signals that will be sent to the Interrupt Matrix.

- GPIO_INTRO
- GPIO_INTR1
- GPIO_INTR2
- GPIO_INTR3
- GPIO_PAD_COMP_INTR

There are several internal interrupt sources from HP IO MUX and HP GPIO matrix that can generate the above interrupt signals. The interrupt sources from HP IO MUX and HP GPIO matrix are listed with their trigger conditions and the resulted interrupt signals in Table 9.18-1. For more detailed information about GPIO_PAD_COMP_INTR, please refer to Chapter 63 Analog Voltage Comparator.

Table 9.18-1. HP IO MUX and HP GPIO Matrix's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
```