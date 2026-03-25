

```markdown
Table 6.15-1. GPIO Pin Analog Functions

| GPIO No. | Pin Name     | Analog Function 0   | Analog Function 1 |
|----------|--------------|--------------------|-------------------|
| 0        | XTAL__32K_P  | XTAL__32K_P        |                   |
| 1        | XTAL__32K_N  | XTAL__32K_N        | ADC1_CH0          |
| 3        | MTMS         | —                  | ADC1_CH1          |
| 4        | MTDI         | —                  | ADC1_CH2          |
| 5        | MTKC         | —                  | ADC1_CH3          |
| 8        | GPIO8        | ZCD0               | —                 |
| 9        | GPIO9        | ZCD1               | —                 |
| 12       | GPIO12       | USB_D-             | —                 |
| 13       | GPIO13       | USB_D+             | —                 |

Note:
* GPIO1 has two different analog functions, which can be used simultaneously.
* ZCD0 and ZCD1 are Analog Voltage Comparator functions. See Chapter 34 Analog Voltage Comparator for details.

6.16 Event Task Matrix Function

In ESP32-C61, GPIO supports ETM function, that is, the ETM task of GPIO can be triggered by the ETM event of any peripheral, or the ETM task of any peripheral can be triggered by the ETM event of GPIO. This section describes only the GPIO-related ETM tasks and events. For a comprehensive description of the ETM system, please refer to 10 Event Task Matrix (ETM).

The GPIO ETM provides eight task channels x (0~7). The ETM tasks that each task channel can receive are:

*   `GPIO_TASK_CHx_SET`: GPIO goes high when triggered.
*   `GPIO_TASK_CHx_CLEAR`: GPIO goes low when triggered.
*   `GPIO_TASK_CHx_TOGGLE`: GPIO toggles level when triggered.

Below is an example to configure task channel x to control GPIOy:

*   Configure IO_MUX_GPIOy_MCU_SEL to 1, to select Function 1 listed in Table 6.13-1.
*   Configure GPIO_ENABLE_REG[y] to 1.
*   Configure GPIO_EXT_ETM_TASK_GPIOy_SEL to x.
*   Set GPIO_EXT_ETM_TASK_GPIOy_EN, to enable ETM task channel x to control GPIOy.

Note:
*   One task channel can be selected by one or more GPIOs.
*   When two or more of the following signals for task channel x: `GPIO_TASK_CHx_SET`, `GPIO_TASK_CHx_CLEAR`, and `GPIO_TASK_CHx_TOGGLE`, are asserted at the same time by GPIOy, the priority is as follows: SET has the highest priority, CLEAR is second, and TOGGLE has the lowest priority.
```