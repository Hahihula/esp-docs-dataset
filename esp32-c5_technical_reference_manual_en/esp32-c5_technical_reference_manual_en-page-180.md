

```markdown
Chapter 4 Low-Power CPU

GoBack

* ULP_TASK_WAKEUP_CPU: Wakes up the LP CPU.
LP CPU can generate the following ETM events:
* ULP_EVT_ERR_INTR: Indicates that an LP CPU exception occurs.
* ULP_EVT_START_INTR: Indicates that the LP CPU clock is turned on.

4.9 Sleep and Wake-Up Process

4.9.1 Features
* Able to sleep, wake up, and operate independently in the low-power system when the HP CPU is working or sleeping
* Able to actively configure registers to enter the sleep status based on software operating status
* Wake-up events:
  - The HP CPU setting the register PMU_HP_TRIGGER_LP
  - The interrupt state of the LP IO
  - ETM events
  - The RTC timer timeout
  - The LP UART receiving a certain number of RX pulses when LPPERI_LP_UART_WAKEUP_EN is enabled

4.9.2 Process
The LP CPU is in sleep by default and its wake-up module follows the process below to wake it up for work and make it sleep.
To configure wake-up sources, please refer to Table 4.9-1.
The first startup of the LP CPU after power-up depends on the wake-up enable and wake-up source configuration by the HP CPU.

* Initialization of the LP CPU
  - Initialize the LP memory.
  - Start the LP CPU. Since the startup of the LP CPU depends on the wake-up process, it is recommended to use the PMU_HP_TRIGGER_LP register to start the initialization of the LP CPU in the following way:
    * Set PMU_LP_CPU_WAKEUP_EN to 0x1
    * Set PMU_HP_TRIGGER_LP to 0x1
    * The LP CPU will go through the wake-up process to start running

* Wake-up process:
  - The wake-up module receives a wake-up signal and sends a power-up request to the PMU.
```