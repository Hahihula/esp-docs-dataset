

```markdown
| LP GPIO No.¹ | GPIO No.¹ | Pin Name   | Analog Function 0 | Analog Function 1 |
|--------------|-----------|------------|-------------------|-------------------|
| 0            | 0         | XTAL_32K_P | XTAL_32K_P        | ADC1_CH0          |
| 1            | 1         | XTAL_32K_N | XTAL_32K_N        | ADC1_CH1          |
| 2            | 2         | GPIO2      | -                 | ADC1_CH2          |
| 3            | 3         | GPIO3      | -                 | ADC1_CH3          |
| 4            | 4         | MTMS       | -                 | ADC1_CH4          |
| 5            | 5         | MTDI       | -                 | ADC1_CH5          |
| 6            | 6         | MTCK       | -                 | ADC1_CH6          |
| -            | 12        | GPIO12²    | USB_D-            | -                 |
| -            | 13        | GPIO13²    | USB_D+            | -                 |

¹ In this table, LP GPIO No. and GPIO No. are used, not the pin No.
² GPIO12 and GPIO13 are not LP GPIO.
```

## 7.14 Event Task Matrix Function

In ESP32-C6, GPIO supports ETM function, that is, the ETM task of GPIO can be triggered by the ETM event of any peripheral, or the ETM task of any peripheral can be triggered by the ETM event of GPIO. For more details about ETM, please refer to Chapter 11 Event Task Matrix (SOC_ETM). Only ETM tasks and ETM events related to GPIO are introduced here.

The GPIO ETM provides eight task channels x (0 ~ 7). The ETM tasks that each task channel can receive are:

*   `GPIO_TASK_CHx_SET`: GPIO goes high when triggered;
*   `GPIO_TASK_CHx_CLEAR`: GPIO goes low when triggered;
*   `GPIO_TASK_CHx_TOGGLE`: GPIO toggle level when triggered.

Below is an example to configure task channel x to control GPIOy:

*   Configure IO_MUX_GPIOy_MCU_SEL to 1, to select Function 1 listed in Table 7.12-1;
*   Configure GPIO_ENABLE_REG[y] to 1;
*   Configure GPIO_EXT_ETM_TASK_GPIOy_SEL to x;
*   Set GPSD_ETM_TASK_GPIOy_EN, to enable ETM task channel x to control GPIOy.
```