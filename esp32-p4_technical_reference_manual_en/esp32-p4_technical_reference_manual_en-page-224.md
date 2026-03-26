

```markdown
| Counter          | Counted Event                                                                 |
|------------------|--------------------------------------------------------------------------------|
| mhpcounter4      | Wait cycles for fetching instructions                                         |
| mhpcounter5      | The number of memory read operations. An unaligned read is counted as two.     |
| mhpcounter6      | The number of memory write operations. An unaligned write is counted as two.   |
| mhpcounter7      | The number of unconditional jump instructions (jal, jr, jalr)                 |
| mhpcounter8      | The number of branch instructions                                              |
| mhpcounter9      | The number of taken branch instructions                                       |
| mhpcounter10     | The number of compressed instructions                                         |
| mhpcounter11     | Wait cycles for multiplication instructions                                   |
| mhpcounter12     | Wait cycles for division instructions                                        |
```

## 3.8 System Access

The LP CPU has access to both memory and peripherals. When accessing an illegal address, i.e., outside the memory’s or peripherals’ address space, it will trigger the corresponding access error exception based on the type of access.

### 3.8.1 Memory Access

The ESP32-P4 LP CPU can access LP ROM, LP SRAM, and L2 SRAM. For more information, please refer to Section 7 System and Memory.

*   LP ROM: 16 KB region starting from `0x5010_0000` to `0x5010_3FFF`. It is used for instruction fetch, data read, etc.
*   LP SRAM: 32 KB region starting from `0x5010_8000` ~ `0x5010_FFFF`. It is used for instruction fetch, data read, data write, etc.
*   L2 SRAM: 768 KB region starting from `0x4FF0_0000` to `0x4FFB_FFFF`. It is used for instruction fetch, data read, data write, etc.

**Note:**
The LP CPU experiences significant latency when accessing L2 SRAM, with each access taking approximately 20 LP CPU clock cycles. However, it can access LP ROM and LP SRAM with no latency.

The LP CPU supports the atomic instruction set. Both the LP CPU and the HP CPU can access memory through atomic instructions, thus achieving atomicity of memory access. For details on the atomic instruction set, please refer to RISC-V Instruction Set Manual Volume I: Unprivileged ISA, Version 2.2.
Note that only L2 SRAM region supports atomic access from HP CPU and LP CPU.

### 3.8.2 Peripheral Access

Table 7.3-2 in Chapter 7 System and Memory lists the peripherals accessible by the LP CPU and their base addresses.
```