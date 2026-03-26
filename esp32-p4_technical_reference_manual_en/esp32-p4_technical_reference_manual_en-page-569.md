

```markdown
| Name       | Analog Function 0          | Analog Function 1 |
|------------|----------------------------|-------------------|
| GPIO18     | ADC1_CHANNEL2              | —                 |
| GPIO19     | ADC1_CHANNEL3              | —                 |
| GPIO20     | ADC1_CHANNEL4              | —                 |
| GPIO21     | ADC1_CHANNEL5              | —                 |
| GPIO22     | ADC1_CHANNEL6              | —                 |
| GPIO23     | ADC1_CHANNEL7              | —                 |
| GPIO24     | USB1P1_NO                  | —                 |
| GPIO25     | USB1P1_PO                  | —                 |
| GPIO26     | USB1P1_N1                  | —                 |
| GPIO27     | USB1P1_P1                  | —                 |
| GPIO49     | ADC2_CHANNEL0              | —                 |
| GPIO50     | ADC2_CHANNEL1              | —                 |
| GPIO51     | ADC2_CHANNEL2              | ANA_COMPO         |
| GPIO52     | ADC2_CHANNEL3              | ANA_COMPO         |
| GPIO53     | ADC2_CHANNEL4              | ANA_COMP1         |
| GPIO54     | ADC2_CHANNEL5              | ANA_COMP1         |

## 9.17 Event Task Matrix Function

In ESP32-P4, GPIO supports ETM function, that is, the ETM task of GPIO can be triggered by the ETM event of any peripheral, or the ETM task of any peripheral can be triggered by the ETM event of GPIO. For more details about ETM, please refer to Chapter 13 Event Task Matrix (ETM). Only ETM tasks and ETM events related to GPIO are introduced here.

The GPIO ETM provides eight task channels x (0 ~ 7). The ETM tasks that each task channel can receive are:

- `GPIO_TASK_CHx_SET`: GPIO goes high when triggered.
- `GPIO_TASK_CHx_CLEAR`: GPIO goes low when triggered.
- `GPIO_TASK_CHx_TOGGLE`: GPIO toggles level when triggered.

Below is an example to configure task channel x to control GPIOy:

- Configure `IO_MUX_GPIOy_MCU_SEL` to 1, to select Function 1 listed in Table 9.14-1.
- Configure `GPIO_ENABLE_REG[y]` to 1.
- Configure `GPIO_EXT_ETM_TASK_GPIOy_SEL` to x.
- Set `GPIO_EXT_ETM_TASK_GPIOy_EN`, to enable ETM task channel x to control GPIOy.

**Note:**

- One task channel can be selected by one or more GPIOs.
- When two or three of the signals `GPIO_TASK_CHx_SET`, `GPIO_TASK_CHx_CLEAR`, and `GPIO_TASK_CHx_TOGGLE` of the task channel x selected by GPIOy are valid at the same time, then `GPIO_TASK_CHx_SET` has the highest priority, `GPIO_TASK_CHx_CLEAR` takes the second higher priority, and `GPIO_TASK_CHx_TOGGLE` has the
```