

```markdown
Register 10.51. HP_SYS_CLKRST_HP_FORCE_NORSTO_REG (0x00CC)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

HP_SYS_CLKRST_FORCE_NORST_COREO   Configures whether HP CPU0 can be reset.
    0: Can be reset
    1: Force not to be reset
    (R/W)

HP_SYS_CLKRST_FORCE_NORST_CORE1   Configures whether HP CPU1 can be reset.
    0: Can be reset
    1: Force not to be reset
    (R/W)

HP_SYS_CLKRST_FORCE_NORST_CORETRACEO   Configures whether RISC-V Trace Encoder 0 can be reset.
    0: Can be reset
    1: Force not to be reset
    (R/W)

HP_SYS_CLKRST_FORCE_NORST_CORETRACE1   Configures whether RISC-V Trace Encoder 1 can be reset.
    0: Can be reset
    1: Force not to be reset
    (R/W)

HP_SYS_CLKRST_FORCE_NORST_L2MEMMON   Configures whether L2 MEM monitor can be reset.
    0: Can be reset
    1: Force not to be reset
    (R/W)

HP_SYS_CLKRST_FORCE_NORST_SPMMON   Configures whether SPM monitor can be reset.
    0: Can be reset
    1: Force not to be reset
    (R/W)
```