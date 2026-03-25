

```markdown
Register 7.90. LP_AON_CPUCOREO_CFG_REG (0x0038)

LP_AON_CPU_COREO_SW_RESET Configures whether to do software reset of the CPU.
    O: Not reset
    1: Reset
        (WT)

LP_AON_CPU_COREO_STAT_VECTOR_SEL Configures whether to start up the CPU from the RTC fast memory.
    O: Do not start up from the RTC fast memory.
    1: Start up from the RTC fast memory.
        (R/W)
```

```markdown
Register 7.91. LPPERI_CLK_EN_REG (0x0000)

LPPERI_EFUSE_CK_EN Configures whether to gate the clock signals of eFuse Controller.
    O: Disable the clock gate
    1: Enable the clock gate
        (R/W)
```