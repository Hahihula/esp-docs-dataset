

```markdown
Register 13.60. LP_AON_CPUCOREO_CFG_REG (0x0038)

| bit | 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----|----|----|----|----|-----|---|
|     |    |    | LP_AON_CPU_COREO_STAT_VECTOR_SEL (reserved) | LP_AON_CPU_COREO_SW_RESET (reserved) | Reset |

LP_AON_CPU_COREO_SW_RESET   Configures CPU Reset.
0: No effect
1: Enable reset
(WT)

LP_AON_CPU_COREO_STAT_VECTOR_SEL   Configures whether to start up the CPU from the LP SRAM.
0: Start up from the LP SRAM.
1: Do not start up from the LP SRAM.
(R/W)
```