

```markdown
Register 10.62. LP_CLKRST_RESET_CAUSE_REG (0x0010)

LP_CLKRST_HPCORE1_RESET_FLAG_CLR
LP_CLKRST_HPCORE1_RESET_CAUSE_CLR
LP_CLKRST_HPCORE1_RESET_FLAG_CLR
LP_CLKRST_HPCORE1_RESET_CAUSE_CLR
LP_CLKRST_HPCORE1_RESET_FLAG_PMU_LP_CPU_MASK

(reserved)

LP_CLKRST_HPCORE1_RESET_FLAG
LP_CLKRST_HPCORE1_RESET_CAUSE

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
|    | 0  | 0  | 0  | 0  | 1   | 0   | 0   | 0   | 0   | 0   | 0x0 | 0   | 0   | 0x0 | Reset |

LP_CLKRST_LPCORE_RESET_CAUSE Represents the reset source of LP CPU.

0x01: Chip reset
0x09: PMU LP Peripheral reset
0x0A: PMU LP CPU reset
0x0F: Brown-out system reset
0x10: RWDT system reset
0x12: Super watchdog reset
0x13: Power glitch reset
0x14: Software LP CPU reset

(RO)

LP_CLKRST_LPCORE_RESET_FLAG Represents the reset flag of LP CPU.

0: Not reset
1: Reset

(RO)
```