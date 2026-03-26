

```markdown
Chapter 10 Reset and Clock

Register 10.62. LP_CLKRST_RESET_CAUSE_REG (0x0010)

Continued from the previous page...

LP_CLKRST_HPCORE1_RESET_CAUSE Represents the reset source of HP CPU1.

0x01: Chip reset
0x03: Software system reset
0x05: PMU core reset
0x07: MWDT core reset
0x09: RWDT core reset
0x0B: MWDT CPU reset
0x0C: Software CPU reset
0x0D: RWDT CPU reset
0xOF: Brown-out system reset
0x10: RWDT system reset
0x12: Super watchdog reset
0x13: Power glitch reset
0x14: eFuse reset
0x16: USB (JTAG) reset
0x17: USB (UART) reset
0x18: JTAG CPU reset
0x1A: Lockup reset
(RO)

LP_CLKRST_HPCORE1_RESET_FLAG Represents the reset flag of HP CPU1.

O: Not reset
1: Reset
(RO)

LP_CLKRST_LPCORE_RESET_CAUSE_PMU_LP_CPU_MASK Configures whether to mask the reset source code 0xOA of PMU LP CPU reset.

O: Not mask
1: Mask
(R/W)

Continued on the next page...
```