

```markdown
Register 10.58. HP_SYS_CLKRST_CPU_WAITI_CTRL0_REG (0x00F4)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| ... |                                                                             |
| 2   | 1                                                                           |
| 1   | 1                                                                           |
| 0   | Reset                                                                       |

HP_SYS_CLKRST_REG_CORE0_WAITI_ICG_EN Configures whether CPU Core0's WAITI signal is used to control the clock gate. 0: Do not use the WAITI signal to control the clock gate. 1: Use the WAITI signal to control the clock gate. If this bit is set for both Core0 and Core1, the related clock is gated only when both Core0's and Core1's WAITI signals are active. (R/W)

HP_SYS_CLKRST_REG_CORE1_WAITI_ICG_EN Configures whether CPU Core1's WAITI signal is used to control the clock gate. 0: Do not use the WAITI signal to control the clock gate. 1: Use the WAITI signal to control the clock gate. If this bit is set for both Core0 and Core1, the related clock is gated only when both Core0's and Core1's WAITI signals are active. (R/W)

10.5.2 LP Always on Clock and Reset (LP_CLKRST) Registers

The addresses in this section are relative to LP_CLKRST base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```