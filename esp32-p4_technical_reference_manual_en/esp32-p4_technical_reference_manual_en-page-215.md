

```markdown
| Interrupt ID | Peripheral Source                     |
|--------------|----------------------------------------|
| 23           | LP_SYSREG_INTR                         |
| 24           | LP_ANAPERI_INTR                        |
| 25           | PMU_REG_O_INTR, PMU_REG_1_INTR         |
| 26           | MB_HP_INTR, MB_LP_INTR                 |
| 27           | LP_TIMER_REG_O_INTR, LP_TIMER_REG_1_INTR |
| 28           | LP_WDT_INTR                            |
| 29           | LP_RTC_INTR                            |
| 30           | HP_INTR                                |

The read-only register `LPINTR_STATUS_REG` indicates the current status of the LP CPU external interrupt sources. For the mapping between this register and the interrupt sources, please refer to the description of this register.

### 3.4.2 Interrupt Handling

By default, interrupts are disabled globally because the MIE bit in `mstatus` has a reset value of 0. Software must set this bit to enable global interrupts.

Assuming the interrupt to enable is Interrupt n:

1. Enable Interrupt n:
   - To enable interrupts globally, write 1 to the MIE bit of `mstatus`.
   - To enable Interrupt n, write 1 to the nth bit of `mie` CSR.
2. After Interrupt n is enabled, the LP CPU can respond to it. Meanwhile, the corresponding peripheral interrupt should be configured to send an interrupt signal to the LP CPU.
3. After the interrupt is triggered, the LP CPU jumps to the `mtvec + 4 * n` address.
4. To clear Interrupt n, the peripheral needs to clear the interrupt signal.

### 3.4.3 Exceptions

The LP CPU supports the RISC-V standard exceptions and can trigger the following exceptions:

**Table 3.4-2. LP CPU Exception Causes**

| Exception ID | Description                          |
|--------------|--------------------------------------|
| 1            | Instruction access fault             |
| 2            | Illegal instructions                |
| 3            | Breakpoints (EBREAK)                 |
| 5            | Load access fault                    |
| 6            | Misaligned atomic instructions       |
| 7            | Store access fault                   |
```