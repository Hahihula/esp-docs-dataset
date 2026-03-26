

```markdown
## 3.4 Interrupts and Exceptions

The LP CPU handles interrupts and exceptions according to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10. After entering an interrupt/exception handler, the CPU:

- Saves the current program counter (PC) value to the `mepc` CSR
- Copies the state of MIE of `mstatus` to MPIE of `mstatus`
- Saves the current privileged mode to MPP of `mstatus`
- Clears MIE of `mstatus`
- Toggles the privileged mode to machine mode (M mode)
- Jumps to the handler address

    - For exceptions, the handler address is the base address of the vector table in the `mtvec` CSR
    - For interrupts, the handler address is `mtvec + 4 * ID`, where ID is the interrupt ID. For more information, see Section 3.4.1

- After the `mret` instruction is executed, the core jumps to the PC saved in the `mepc` CSR, restores the value of MPIE of `mstatus` to MIE of `mstatus`, and restores the privileged mode to that indicated by MPP of `mstatus`

When the core starts up, the base address of the vector table is initialized to the boot address 0x50000000. After startup, the base address can be changed by writing to the `mtvec` CSR. For more information about CSRs, see Section 3.3.1.

After a reset, the core starts to fetch instructions from the memory address specified by the `LP_SYS_LP_CORE_BOOT_ADDR_REG` register with an offset of 0x80. The default value for this register is 0x50100000, which corresponds to the starting address of the LP ROM.

## 3.4.1 Interrupts

The LP CPU in the ESP32-P4 supports 18 interrupt inputs. Each interrupt corresponds to an ID, which is denoted as `n` (where `n = 3, 7, 11, 16 to 30`), and has a specific entry address of `mtvec + 4 * n`. These interrupts are associated with specific peripheral sources. For the mapping between peripheral sources and interrupt IDs, please refer to 3.4-1.

Table 3.4-1. LP CPU Interrupt Mapping

| Interrupt ID | Peripheral Source        |
|--------------|--------------------------|
| 3            | LP_SW_INTR               |
| 7            | LP_UART_INTR             |
| 11           | LP_SPI_INTR              |
| 17           | LP_I2C_INTR              |
| 18           | LP_GPIO_INTR             |
| 19           | LP_ADC_INTR              |
| 20           | LP_TOUCH_INTR            |
| 21           | LP_TSENS_INTR            |
| 22           | LP_EFUSE_INTR            |
```