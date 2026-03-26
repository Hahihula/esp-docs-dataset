

```markdown
Chapter 10 Reset and Clock

Register 10.63. LP_CLKRST_HPCPU_RESET_CTRL0_REG (0x0014)

Continued from the previous page...

LP_CLKRST_HPCORE0_STAT_VECTOR_SEL Configures the address from which the HP CPU0 starts.
    0: From LP SPM RAM (0x50108000)
    1: From HP SPM ROM (0x4FC00000)
    (R/W)

LP_CLKRST_HPCORE1_LOCKUP_RESET_EN Configures whether to enable Lockup to trigger HP CPU1 reset.
    0: Disable
    1: Enable
    (R/W)

LP_CLKRST_LP_WDT_HPCORE1_RESET_LENGTH Configures the duration of the reset when RWDT and software trigger HP CPU1 reset.
Measurement unit: Clock cycles. (R/W)

LP_CLKRST_LP_WDT_HPCORE1_RESET_EN Configures whether to enable RWDT to trigger HP CPU1 reset.
    0: Disable
    1: Enable
    (R/W)

LP_CLKRST_HPCORE1STALL_WAIT Configures the time HP CPU1 stalls when RWDT and software trigger HP CPU1 reset.
Measurement unit: Clock cycles. (R/W)

LP_CLKRST_HPCORE1STALL_EN Configures the behavior when RWD T and software trigger HP CPU1 reset.
    0: Immediately reset HP CPU1
    1: Stall HP CPU1 first
    (R/W)

LP_CLKRST_HPCORE1_SW_RESET Write 1 to trigger HP CPU1 software reset. (WT)

LP_CLKRST_HPCORE1_OCD_HALT_ON_RESET Configures whether HP CPU1 halts at the first instruction after released from reset.
    0: No halt
    1: Halt
    (R/W)

LP_CLKRST_HPCORE1_STAT_VECTOR_SEL Configures the address from which the HP CPU1 starts.
    0: From LP SPM RAM (0x50108000)
    1: From HP SPM ROM (0x4FC00000)
    (R/W)
```