
```markdown
## 3.9 Event Task Matrix Feature

The LP CPU on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows LP CPU’s ETM tasks to be triggered by any peripherals’ ETM events, or LP CPU’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to the LP CPU. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

LP CPU can receive the following ETM task:

*   ULP_TASK_WAKEUP_CPU: Wakes up the LP CPU.
*   ULP_TASK_INT_CPU: Triggers an LP CPU interrupt.

LP CPU can generate the following ETM events:

*   ULP_EVT_ERR_INTR: Indicates that an LP CPU exception occurs.
*   ULP_EVT_START_INTR: Indicates that the LP CPU clock is turned on.
*   ULP_EVT_HALT: Indicates that the LP CPU enters the sleep state

## 3.10 Sleep and Wake-Up Process

### 3.10.1 Features

Here are the sleep and wake-up features supported by the LP CPU.

*   Independent operation, sleeping, and waking-up in the low-power system when the HP CPU is sleeping
*   Actively configuring registers to enter the sleep state based on software operating status
*   Multiple wake-up sources
*   Sleep entry rejection by peripherals

### 3.10.2 Process

The LP CPU is in sleep by default and its wake-up module follows the process below to wake it up for work and make it sleep.

To configure wake-up sources, please refer to Table 3.10-1.

The first startup of the LP CPU after power-up depends on the wake-up enable and wake-up source configuration by the HP CPU.

*   Initialization of the LP CPU
    *   Initialize the LP memory.
    *   Start the LP CPU. Since the startup of the LP CPU depends on the wake-up process, it is recommended to use the PMU_HP_TRIGGER_LP register to start the initialization of the LP CPU in the following way:
        *   Set PMU_LP_CPU_WAKEUP_EN to 0x400000
        *   Set PMU_HP_TRIGGER_LP to 0x1
```