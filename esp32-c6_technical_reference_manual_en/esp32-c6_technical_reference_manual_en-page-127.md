

```markdown
LP CPU can generate the following ETM events:

*   ULP_EVT_ERR_INTR: Indicates that an LP CPU exception occurs.
*   ULP_EVT_START_INTR: Indicates that the LP CPU clock is turned on.

## 3.9 Sleep and Wake-Up Process

### 3.9.1 Features

*   Able to sleep, wake up, and operate independently in the low-power system when the HP CPU is sleeping
*   Able to actively configure registers to enter the sleep status based on software operating status
*   Wake-up events:
    *   The HP CPU setting the register PMU_HP_TRIGGER_LP
    *   The interrupt state of the LP IO
    *   ETM events
    *   The RTC timer timeout
    *   The LP UART receiving a certain number of RX pulses when LPPERI_LP_UART_WAKEUP_EN is enabled

### 3.9.2 Process

The LP CPU is in sleep by default and its wake-up module follows the process below to wake it up for work and make it sleep.

To configure wake-up sources, please refer to Table 3.9-1.
```

![Figure 3.9-1. Wake-Up and Sleep Flow of LP CPU](image_description_not_provided)

```markdown
PMU_LP_CPU_SLP_STALL_EN == 1  
PMU_LP_CPU_SLP_STALL_EN == 0  

PMU_LP_CPU_SLP_BYPASS_INTR_EN == 1  
PMU_LP_CPU_SLP_BYPASS_INTR_EN == 0  

PMU_LP_CPU_SLP_RESET_EN == 1  
PMU_LP_CPU_SLP_RESET_EN == 0
```