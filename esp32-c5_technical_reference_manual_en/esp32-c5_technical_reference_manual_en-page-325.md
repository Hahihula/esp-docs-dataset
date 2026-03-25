

```markdown
| LP IO Name | Function 0             | Function 1*       | Function 2 | Function 3 |
|------------|------------------------|-------------------|----------|----------|
| GPIO4      | LP_UART_RXD_PAD        | LP_GPIO4          | —        | —        |
| GPIO5      | LP_UART_TXD_PAD        | LP_GPIO5          | —        | —        |
| GPIO6      | —                      | LP_GPIO6          | —        | —        |

**Notice:**
* Hardware flow control of LP_UART cannot be used with LP_I2C at the same time.
* In LP IO MUX, unused pins must be configured to LP_GPIO function.
* This column lists the LP GPIO names, since LP functions are configured with LP GPIO registers that use LP GPIO numbering.

## 8.15 GPIO Pin Analog Function List

Table 8.15-1 shows the GPIO pins and their corresponding analog functions.

**Table 8.15-1. GPIO Pin Analog Functions**

| Name       | Analog Function 0   | Analog Function 1 |
|------------|---------------------|-------------------|
| XTAL_32K_P | XTAL_32K_P          |                   |
| XTAL_32K_N | XTAL_32K_N          | ADC1_CH0          |
| MTMS       | —                   | ADC1_CH1          |
| MTDI       | —                   | ADC1_CH2          |
| MTCK       | —                   | ADC1_CH3          |
| MTDO       | —                   | ADC1_CH4          |
| GPIO6      | —                   | ADC1_CH5          |
| GPIO8      | ZCD0*               | —                 |
| GPIO9      | ZCD1*               | —                 |
| GPIO13     | USB_D-              | —                 |
| GPIO14     | USB_D+              | —                 |

\* ZCD0 and ZCD1 are analog PAD voltage comparator functions. See Chapter 47 Analog Voltage Comparator for details.

## 8.16 Event Task Matrix Function

In ESP32-C5, GPIO supports ETM function, that is, the ETM task of GPIO can be triggered by the ETM event of any peripheral, or the ETM task of any peripheral can be triggered by the ETM event of GPIO. For more details about ETM, please refer to Chapter 12 Event Task Matrix (ETM). Only ETM tasks and ETM events related to GPIO are introduced here.

The GPIO ETM provides eight task channels x (0~7). The ETM tasks that each task channel can receive are:

* GPIO_TASK_CHx_SET: GPIO goes high when triggered.
```