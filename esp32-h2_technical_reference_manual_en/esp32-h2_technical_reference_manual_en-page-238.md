

```markdown
- Configure GPIO_EXT_ETM_TASK_GPIOy_SEL to x;
- Set GPIO_EXT_ETM_TASK_GPIOy_EN, to enable ETM task channel x to control GPIOy.

Note:
- One task channel can be selected by one or more GPIOs.
- When two or three of the signals GPIO_TASK_CHx_SET, GPIO_TASK_CHx_CLEAR, and GPIO_TASK_CHx_TOGGLE of the task channel x selected by GPIOy are valid at the same time, then GPIO_TASK_CHx_SET has the highest priority, GPIO_TASK_CHx_CLEAR takes the second higher priority, and GPIO_TASK_CHx_TOGGLE has the lowest priority.
- When GPIOy is controlled by ETM task channel, the values of GPIO_OUT_REG, GPIO_FUNCn_OUT_INV_SEL, and GPIO_FUNCn_OUT_SEL may be modified by the hardware. For such reason, it's recommended to reconfigure these registers when the GPIO is free from the control of ETM task channel.

GPIO has eight event channels, and the ETM events that each event channel can generate are:

- GPIO_EVT_CHx_RISE_EDGE: Indicates that the output signal of the corresponding GPIO filter (see Figure 6.3-1) has a rising edge;
- GPIO_EVT_CHx_FALL_EDGE: Indicates that the output signal of the corresponding GPIO filter (see Figure 6.3-1) has a falling edge;
- GPIO_EVT_CHx_ANY_EDGE: Indicates that the output signal of the corresponding GPIO filter (see Figure 6.3-1) is reversed.

The specific configuration of the event channel is as follows:

- Set GPIO_EXT_ETM_CHx_EVENT_EN to enable event channel x (0 ~ 7).
- Configure GPIO_EXT_ETM_CHx_EVENT_SEL to y (0 ~ 5, 8 ~ 14 and 22 ~ 27), i.e., select one from the 19 GPIOs.

Note:
One GPIO can be selected by one or more event channels.
```