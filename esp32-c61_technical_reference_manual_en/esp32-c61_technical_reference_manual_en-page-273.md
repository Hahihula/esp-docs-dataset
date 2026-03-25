

```markdown
- When GPIOy is controlled by ETM task channel, the values of GPIO_OUT_REG, GPIO_FUNCy_OUT_INV_SEL, and GPIO_FUNCy_OUT_SEL may be modified by the hardware. For such reason, it's recommended to reconfigure these registers when the GPIO is free from the control of ETM task channel.
```

GPIO has eight event channels, and the ETM events that each event channel can generate are:

- GPIO_EVT_CHx_RISE_EDGE: The output signal of the corresponding GPIO Filter (see Figure 6.3-1) has a rising edge.
- GPIO_EVT_CHx_FALL_EDGE: The output signal of the corresponding GPIO Filter (see Figure 6.3-1) has a falling edge.
- GPIO_EVT_CHx_ANY_EDGE: The output signal of the corresponding GPIO Filter (see Figure 6.3-1) is reversed.

The specific configuration of the event channel is as follows:

- Set GPIO_EXT_ETM_CHx_EVENT_EN to enable event channel x (0~7).
- Configure GPIO_EXT_ETM_CHx_EVENT_SEL to y (0~13, 22~29), i.e., select one from the 22 GPIOs.

Note:
One GPIO can be selected by one or more event channels.

In some applications, GPIO ETM events can be used to trigger GPIO ETM tasks. For example, event channel 0 selects GPIO0, GPIO1 selects task channel 0, and the GPIO_EVT_CH0_RISE_EDGE event is used to trigger the GPIO_TASK_CH0_TOGGLE task. When a square wave signal is input to the chip through GPIO0, the chip outputs a square wave signal with a frequency divided by 2 through GPIO1.

## 6.17 Interrupts

ESP32-C61's HP IO MUX and HP GPIO matrix can generate the following interrupt signals that will be sent to the Interrupt Matrix.

- GPIO_EXT_REG_INT
- GPIO_PROCPU_INT

Several internal interrupt sources from HP IO MUX and HP GPIO matrix can generate the above interrupt signals. Table 6.17-1 lists the interrupt sources from HP IO MUX and HP GPIO matrix with their trigger conditions and the resulted interrupt signals.

Table 6.17-1. HP IO MUX and HP GPIO Matrix's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|----------------------------|-------------------|------------------|
| GPIO_EXT_COMP_ALL_O_INT   | See Chapter 34 Analog Voltage Comparator | GPIO_EXT_REG_INT |
| GPIO_EXT_COMP_NEG_O_INT   | See Chapter 34 Analog Voltage Comparator | GPIO_EXT_REG_INT |
| GPIO_EXT_COMP_POS_O_INT   | See Chapter 34 Analog Voltage Comparator | GPIO_EXT_REG_INT |
```