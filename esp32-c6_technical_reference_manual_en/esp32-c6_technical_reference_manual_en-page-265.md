

```markdown
Note:

* One task channel can be selected by one or more GPIOs.
* When two or three of the signals `GPIO_TASK_CHx_SET`, `GPIO_TASK_CHx_CLEAR`, and `GPIO_TASK_CHx_TOGGLE` of the task channel x selected by `GPIOy` are valid at the same time, then `GPIO_TASK_CHx_SET` has the highest priority, `GPIO_TASK_CHx_CLEAR` takes the second higher priority, and `GPIO_TASK_CHx_TOGGLE` has the lowest priority.
* When `GPIOy` is controlled by ETM task channel, the values of `GPIO_OUT_REG`, `GPIO_FUNCn_OUT_INV_SEL`, and `GPIO_FUNCn_OUT_SEL` may be modified by the hardware. For such reason, it's recommended to reconfigure these registers when the GPIO is free from the control of ETM task channel.

GPIO has eight event channels, and the ETM events that each event channel can generate are:

* `GPIO_EVT_CHx_RISE_EDGE`: Indicates that the output signal of the corresponding GPIO filter (see Figure 7.3-1) has a rising edge;
* `GPIO_EVT_CHx_FALL_EDGE`: Indicates that the output signal of the corresponding GPIO filter (see Figure 7.3-1) has a falling edge;
* `GPIO_EVT_CHx_ANY_EDGE`: Indicates that the output signal of the corresponding GPIO filter (see Figure 7.3-1) is reversed.

The specific configuration of the event channel is as follows:

* Set `GPIO_EXT_ETM_CHx_EVENT_EN` to enable event channel x (0 ~ 7).
* Configure `GPIO_EXT_ETM_CHx_EVENT_SEL` to y (0 ~ 30), i.e., select one from the 31 GPIOs.

Note:
One GPIO can be selected by one or more event channels.
```

## 7.15 Register Summary

### 7.15.1 GPIO Matrix Register Summary

The addresses in this section are relative to GPIO base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Note:** For chip variants with an in-package flash, 22 GPIO pins are available, i.e., `GPIO0 ~ GPIO9` and `GPIO12 ~ GPIO23`. For this case:

* Configuration Registers: can only be configured for `GPIO0 ~ GPIO9` and `GPIO12 ~ GPIO23`.
```