

```markdown
## 4.3.1 Interrupts

The ESP32-C5 LP CPU supports only one interrupt entry, to which all interrupt events jump. The LP CPU supports the following peripheral interrupt sources:

* Power Management Unit (PMU)
* Low-Power Timer (RTC_TIMER)
* Low-Power UART (LP_UART)
* Low-Power I2C (LP_I2C)
* Low-Power IO MUX (LP_IO_MUX)

For more information on those peripheral interrupts, please refer to the corresponding chapter.

## 4.3.2 Interrupt Handling

By default, interrupts are disabled globally because the MIE bit in mstatus has a reset value of 0. Software must set this bit to enable global interrupts.

1. Enable interrupts
    * To enable interrupts globally, set the MIE bit of mstatus.
    * To enable Interrupt 30, set the 30th bit of mie CSR.
2. After interrupts are enabled, the LP CPU can respond to interrupts. It also needs to configure interrupts of the peripherals so that they can send an interrupt signal to the LP CPU.
3. After the interrupt is triggered, the LP CPU jumps to `mtvec + 4 * 30`.
4. After entering the interrupt handler, users need to read `LPPERI_INTERRUPT_SOURCE_REG` to get the peripheral that triggered the interrupt and process the interrupt. Note that if the interrupts are triggered by multiple peripherals, the CPU will process them one by one in sequence until none is left. If not all interrupts are processed, the CPU will enter the interrupt handler again.
5. To clear interrupts, just clear the interrupt signal of the peripheral.

## 4.3.3 Exceptions

The LP CPU supports the RISC-V standard exceptions and can trigger the following exceptions:

Table 4.3-1. LP CPU Exception Causes

| Exception ID | Description                     |
|--------------|----------------------------------|
| 2            | Illegal instructions             |
| 3            | Breakpoints (EBREAK)              |
| 6            | Misaligned atomic instructions    |
```