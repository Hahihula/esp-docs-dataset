

```markdown
| PMU_nDIG_ICG_FUNC_EN Bit | Clock |
|---------------------------|-------|
| bit 20                    | L1CACHE_I1_MEM_CLK |
| bit 21                    | L2CACHE_MEM_CLK    |
| bit 22                    | L2CACHE_SYS_CLK    |
| bit 23                    | REGDMA_SYS_CLK     |
| bit 24                    | HP_CLKRST_APB_CLK  |
| bit 25                    | SYSREG_APB_CLK     |
| bit 26                    | INTRMTX_CLK        |
| bit 27                    | N/A                 |
| bit 28                    | N/A                 |
| bit 29                    | N/A                 |
| bit 30                    | N/A                 |
| bit 31                    | N/A                 |

The LP system clocks are mainly used in the low-power system and include the following clocks:

*   LP_SLOW_CLK
*   LP_FAST_CLK
*   LP_DYN_SLOW_CLK
*   LP_DYN_FAST_CLK
*   XTAL_D2_CLK

The clock frequency of LP_DYN_FAST_CLK is controlled by hardware as follows, depending on the PMU state (and cannot be changed by the user):

*   LP_SLEEP: The LP_DYN_FAST_CLK frequency is the same as LP_SLOW_CLK.
*   HP_ACTIVE, HP_SLEEP: The LP_DYN_FAST_CLK frequency is the same as LP_FAST_CLK.

### 14.4.2.6 Backup Controller

ESP32-P4 has a Retention DMA module that can transfer data between memory and peripherals when the chip switches between PMU states. In this way, the data is backed up when the power domain is powered down and restored when the power domain is powered up again.

Data transfer is implemented in the Peripherals power domain. PMU only generates relevant control signals. It is important to note that the data transfer control registers are directional, as unlike other control registers, these control behaviors are determined by both the original PMU state and the target PMU state.

For example, the control registers for transitioning from HP_ACTIVE to HP_SLEEP and from HP_SLEEP to HP_ACTIVE are different. The possible PMU state switches are listed below, collectively represented by `n2` in the register names:

*   HP_SLEEP2ACTIVE
*   HP_ACTIVE2SLEEP

The following section introduces how PMU controls the Retention DMA:
```