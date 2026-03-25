
```markdown
- LP_DYN_SLOW_CLK is clk_root_slow_gated, which is generated from LP_DYN_FAST_CLK through a clock gate. The enable signal of the clock gate is controlled by the rising edge of LP_DYN_SLOW_CLK after being synchronized through a double flip-flop.

11.4.2.6 Backup Controller

ESP32-C61 has a Retention DMA module, which is in the “ROM + Peripherals” power domain, that can transfer data between memory and peripherals when the chip switches between PMU states, so that the data is backed up when the power domain is powered down and restored when the power domain is powered up again.

Data transfer is implemented via REGDMA. PMU only generates relevant control signals. It is important to note that the data transfer control registers are directional, as unlike other control registers, these control behaviors are determined by both the original PMU state and the target PMU state.

Take the HP_SLEEP target PMU state as an example, the control registers for transitioning from HP_ACTIVE to HP_SLEEP and from HP_MODEM to HP_SLEEP are different. The possible PMU state switches are listed below, collectively represented by PMUSTATE_TRANS in the register names:

*   HP_SLEEP2ACTIVE
*   HP_SLEEP2MODEM
*   HP_MODEM2ACTIVE
*   HP_MODEM2SLEEP
*   HP_ACTIVE2SLEEP

All such registers are linked to a representative of the same type for reference. For example, PMU_PMUSTATE_TRANS_BACKUP_EN will be linked to PMU_HP_SLEEP2ACTIVE_BACKUP_EN.

The following will introduce how PMU controls the Retention DMA:

*   Enable data transfer: Configure PMU_PMUSTATE_TRANS_BACKUP_EN to 1 to enable data transfer when the corresponding PMU state switch is performed.
*   Enable corresponding clocks: Before data transfer starts, configure PMU_PMUSTATE_TRANS_BACKUP_CLK_SEL to select the clock source of the Retention DMA, and configure PMU_PMUSTATE_BACKUP_ICG_FUNC_EN to enable the clock.

After the data transfer is completed, the value of PMU_PMUSTATE_BACKUP_ICG_FUNC_EN is determined by the configuration of PMU_PMUSTATE_DIG_ICG_FUNC_EN in the target PMU state.

*   Configure data transfer direction: Configure the highest bit of PMU_PMUSTATE_TRANS_BACKUP_MODE:

    - 1: From peripheral to memory
    - 0: From memory to peripheral

*   Select linked list pointer: Configure the lower two bits of PMU_PMUSTATE_TRANS_BACKUP_MODE to select the linked list pointer, specifically:

    - 0: PAU_LINK_ADDR_0
    - 1: PAU_LINK_ADDR_1
    - 2: PAU_LINK_ADDR_2
```