

```markdown
Register 10.48. HP_SYS_CLKRST_HP_RST_ENO_REG (0x00C0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

HP_SYS_CLKRST_RST_EN_CORECTRL Configures whether to reset CORECTRL.
- 0: Release from reset
- 1: Reset
(R/W)

HP_SYS_CLKRST_RST_EN_COREO_GLOBAL Configures whether to reset HP CPU0.
- 0: Release from reset
- 1: Reset
(R/W)

HP_SYS_CLKRST_RST_EN_CORE1_GLOBAL Configures whether to reset HP CPU1.
- 0: Release from reset
- 1: Reset
(R/W)

HP_SYS_CLKRST_RST_EN_CORETRACEO Configures whether to reset RISC-V Trace Encoder0.
- 0: Release from reset
- 1: Reset
(R/W)

HP_SYS_CLKRST_RST_EN_CORETRACE1 Configures whether to reset RISC-V Trace Encoder1.
- 0: Release from reset
- 1: Reset
(R/W)

HP_SYS_CLKRST_RST_EN_HP_SPM Configures whether to reset SPM.
- 0: Release from reset
- 1: Reset
(R/W)
```