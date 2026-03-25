

```markdown
| PMU_n1_DIG_ICG_APB_EN Bit | Clock                     |
|----------------------------|---------------------------|
| bit 3                      | INTMTX_APB_CLK            |
| bit 4                      | I2S_APB_CLK               |
| bit 5                      | MSPI_APB_CLK              |
| bit 6                      | UART0_APB_CLK             |
| bit 7                      | UART1_APB_TX_CLK          |
| bit 8                      | UHCI_APB_CLK              |
| bit 9                      | SARADC_APB_CLK            |
| bit 10                     | N/A                       |
| bit 11                     | TimerGroup0_APB_CLK       |
| bit 12                     | TimerGroup1_APB_CLK       |
| bit 13                     | I2C_APB_CLK               |
| bit 14                     | LEDC_APB_CLK              |
| bit 15                     | RMT_APB_CLK               |
| bit 16                     | SYSTIMER_APB_CLK          |
| bit 17                     | USB_DEVICE_APB_CLK        |
| bit 18                     | TWAIO_APB_CLK             |
| bit 19                     | N/A                       |
| bit 20                     | PCNT_APB_CLK              |
| bit 21                     | PWM_APB_CLK               |
| bit 22                     | SOC_ETM_CLK               |
| bit 23                     | PARLIO_APB_CLK            |
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
*   HP_ACTIVE, HP_SLEEP: The LP_DYN_FAST_CLK frequency is the same as LP_FAST_CLK.
```