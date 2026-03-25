

```markdown
11.4.2.6 Backup Controller

ESP32-H2 has a Retention DMA module that can transfer data between memory and peripherals when the chip switches between PMU states, so that the data is backed up when the power domain is powered down and restored when the power domain is powered up again.

Data transfer is implemented in the Peripherals power domain. PMU only generates relevant control signals. It is important to note that the data transfer control registers are directional, as unlike other control registers, these control behaviors are determined by both the original PMU state and the target PMU state. Since the basic configurations of the Retention DMA are in the Peripherals power domain, if you want to use the Retention DMA in sleep modes, do not power down the Peripherals power domain.

Taking the HP_SLEEP target PMU state as an example, the control registers for transitioning from HP_ACTIVE to HP_SLEEP and from HP_SLEEP to HP_ACTIVE are different. The possible PMU state switches are listed below, collectively represented by n2 in the register names:

*   HP_SLEEP2ACTIVE
*   HP_ACTIVE2SLEEP

The following will introduce how PMU controls the Retention DMA:

*   Enable data transfer: Configure PMU_n2_BACKUP_EN to 1 to enable data transfer when the corresponding PMU state switch is performed.
*   Enable corresponding clocks: Before data transfer starts, configure PMU_n2_BACKUP_CLK_SEL to select the clock source of the Retention DMA, and configure PMU_n1_BACKUP_ICG_FUNC_EN to enable the clock.

After the data transfer is completed, the value of PMU_n1_BACKUP_ICG_FUNC_EN is determined by the configuration of PMU_n1_DIG_ICG_FUNC_EN in the target PMU state.
*   Configure data transfer direction: Configure the highest bit of PMU_n2_BACKUP_MODE:
    - 1: From peripheral to memory
    - 0: From memory to peripheral
*   Select linked list pointer: Configure the lower two bits of PMU_n2_BACKUP_MODE to select the linked list pointer, specifically:
    - 0: PAU_LINK_ADDR_0
    - 1: PAU_LINK_ADDR_1
    - 2: PAU_LINK_ADDR_2
    - 3: PAU_LINK_ADDR_3

11.4.2.7 System Controller

The system controller controls some functional modules when the chip switches PMU states, to achieve stable and low-power chip performance. Specifically, the system controller supports:

*   Pausing the watchdog function: Configuring PMU_n1_DIG_PAUSE_WDT to 1 can disable the RTC watchdog timer (RWDT) function when the chip switches to the corresponding target PMU state. Note
```