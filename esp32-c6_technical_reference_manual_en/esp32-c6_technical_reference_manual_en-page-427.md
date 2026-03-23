

```markdown
| PMU_n1_DIG_ICG_APB_EN Bit | Clock                     |
|----------------------------|---------------------------|
| bit 24                     | REGDMA_APB_CLK            |
| bit 25                     | MEMORY_MONITOR_APB_CLK    |
| bit 26                     | IOMUX_APB_CLK             |
| bit 27                     | PVT_APB_CLK               |
| bit 28                     | N/A                       |
| bit 29                     | N/A                       |
| bit 30                     | N/A                       |
| bit 31                     | N/A                       |

LP system clocks are mainly used in the low-power system and include the following four clocks:

*   LP_SLOW_CLK
*   LP_FAST_CLK
*   LP_DYN_SLOW_CLK
*   LP_DYN_FAST_CLK

The clock frequency of LP_DYN_FAST_CLK is controlled by hardware as follows, depending on the PMU state (and cannot be changed by the user):

*   LP_SLEEP: The LP_DYN_FAST_CLK frequency is the same as LP_SLOW_CLK.
*   HP_ACTIVE, HP_MODEM, HP_SLEEP: The LP_DYN_FAST_CLK frequency is the same as LP_FAST_CLK.

### 12.4.2.6 Backup Controller

ESP32-C6 has a Retention DMA module that can transfer data between memory and peripherals when the chip switches between PMU states, so that the data is backed up when the power domain is powered down and restored when the power domain is powered up again.

Data transfer is implemented in the Peripherals power domain. PMU only generates relevant control signals. It is important to note that the data transfer control registers are directional, as unlike other control registers, these control behaviors are determined by both the original PMU state and the target PMU state.

Taking the HP_SLEEP target PMU state as an example, the control registers for transitioning from HP_ACTIVE to HP_SLEEP and from HP_MODEM to HP_SLEEP are different. The possible PMU state switches are listed below, collectively represented by `n2` in the register names:

*   HP_SLEEP2ACTIVE
*   HP_SLEEP2MODEM
*   HP_MODEM2ACTIVE
*   HP_MODEM2SLEEP
*   HP_ACTIVE2SLEEP

The following will introduce how PMU controls the Retention DMA:

*   Enable data transfer: Configure `PMU_n2_BACKUP_EN` to 1 to enable data transfer when the corresponding PMU state switch is performed.
```