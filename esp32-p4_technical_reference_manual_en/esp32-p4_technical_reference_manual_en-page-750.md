

```markdown
|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
||0|0| | | ||||||||||||||||Reset|

LP_CLKRST_HPCOREO_LOCKUP_RESET_EN Configures whether to enable Lockup to trigger HP CPU0 reset.
0: Disable
1: Enable (R/W)

LP_CLKRST_LP_WDT_HPCOREO_RESET_LENGTH Configures the duration of the reset when RWDT and software trigger HP CPU0 reset.
Measurement unit: Clock cycles. (R/W)

LP_CLKRST_LP_WDT_HPCOREO_RESET_EN Configures whether to enable RWDT to trigger HP CPU0 reset.
0: Disable
1: Enable (R/W)

LP_CLKRST_HPCOREO_STALL_WAIT Configures the time HP CPU0 stalls when RWDT and software trigger HP CPU0 reset.
Measurement unit: Clock cycles. (R/W)

LP_CLKRST_HPCOREO_STALL_EN Configures the behavior when RWDT and software trigger HP CPU0 reset.
0: Immediately reset HP CPU0
1: Stall HP CPU0 first (R/W)

LP_CLKRST_HPCOREO_SW_RESET Write 1 to trigger HP CPU0 software reset. (WT)

LP_CLKRST_HPCOREO_OCD_HALT_ON_RESET Configures whether HP CPU0 halts at the first instruction after released from reset.
0: No halt
1: Halt (R/W)
```