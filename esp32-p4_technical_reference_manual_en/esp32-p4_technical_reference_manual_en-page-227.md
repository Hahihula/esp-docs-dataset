

```markdown
# Chapter 3 Low-Power CPU

## 3.10.3 Wake-Up Sources

Table 3.10-1. Wake Sources  

| Register Value¹ | Wake-Up Source       | Description                                                                                                                                                                                                 |
|------------------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BIT(9)           | LP IO                | The LP CPU can be waken up by the LP IO interrupt status register signal. For more information, please refer to Chapter 9 GPIO Matrix and IOMUX.                                                               |
| BIT(10)          | LP UART              | The LP CPU can be waken up when the LP UART receives a certain number of RX pulses. REG_UART_WAKEUP_EN needs to be enabled. For more information, please refer to Chapter 42 UART Controller (UART).                                                                 |
| BIT(13)          | RTC timer            | The LP CPU can be waken up by the RTC timer target 0 timeout interrupt. For more information, please refer to Chapter 14 Low-Power Management.                                                                     |
| BIT(14)          | Brownout detection   | The LP CPU can be waken up when a brownout occurs. For more information, please refer to Chapter 23 Brown-out Detector.                                                                                      |
| BIT(17)          | ETM                  | The LP CPU can be waken up by the ETM task. For more information, please refer to Chapter 13 Event Task Matrix (ETM).                                                                                        |
| BIT(18)          | RTC timer            | The LP CPU can be waken up by the RTC timer target 0 timeout interrupt. For more information, please refer to Chapter 14 Low-Power Management.                                                                     |
| BIT(19)          | LP I2S audio         | The LP CPU can be waken up when the predefined audio is received via I2S. For more details, please refer to Chapter 46 I2S Controller (I2S).                                                                       |
| BIT(22)          | PMU_HP_TRIGGER_LP register | The HP CPU sets the register PMU_HP_TRIGGER_LP to wake up the LP CPU, and sets REG_HP_SW_TRIGGER_INT_CLR to clear this wake-up source.                                                                         |

¹ Value of the **PMU_LP_CPU_WAKEUP_EN** register


## 3.10.4 Sleep Rejection

When the LP CPU is preparing to enter the sleep state, it can be rejected by peripheral events. In other words, peripheral events have the capability to prevent the LP CPU from entering sleep mode. Below is the configuration process for the rejection:

1. The LP CPU configures **PMU_SLP_REJECT_EN** to enable the functionality that allows peripherals to reject the LP CPU from entering the sleep mode.
2. The LP CPU configures **PMU_SLEEP_REJECT_ENA** to enable the corresponding peripheral event to prevent the LP CPU from entering the sleep state.

The peripheral sources that can prevent the LP CPU from sleeping are the same as the wake-up sources.
```