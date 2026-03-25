

```markdown
| Counter               | Counted Event                                                                 |
|-----------------------|--------------------------------------------------------------------------------|
| mhpmmcounter4         | Wait cycles for fetching instructions                                         |
| mhpmmcounter5         | The number of memory read operations. An unaligned read is counted as two.      |
| mhpmmcounter6         | The number of memory write operations. An unaligned write is counted as two.    |
| mhpmmcounter7         | The number of unconditional jump instructions (jal, jr, jalr)                  |
| mhpmmcounter8         | The number of branch instructions                                              |
| mhpmmcounter9         | The number of taken branch instructions                                       |
| mhpmmcounter10        | The number of compressed instructions                                         |
| mhpmmcounter11        | Wait cycles for multiplication instructions                                   |
| mhpmmcounter12        | Wait cycles for division instructions                                        |

## 4.7 System Access

### 4.7.1 Memory Access

The ESP32-C5 LP CPU can access LP SRAM and HP SRAM. For more information, please refer to Section 6 System and Memory.

*   LP SRAM: 16 KB starting from 0x5000_0000 to 0x5000_3FFF, where you can fetch instructions, read data, write data, etc.
*   HP SRAM: 384 KB starting from 0x4080_0000 to 0x4085_FFFF, where you can fetch instructions, read data, write data, etc.

**Note:**
The LP CPU has a high latency to access the HP SRAM, but can access the LP SRAM with no latency.

The LP CPU supports the atomic instruction set. Both the LP CPU and the HP CPU can access memory through atomic instructions, thus achieving atomicity of memory access. For details on the atomic instruction set, please refer to RISC-V Instruction Set Manual Volume I: Unprivileged ISA, Version 2.2.
Note that only HP SRAM supports atomic access from HP CPU and LP CPU.

### 4.7.2 Peripheral Access

Table 6.3-2 in Chapter 6 System and Memory lists the peripherals accessible by the LP CPU and their base addresses.

## 4.8 Event Task Matrix Feature

The LP CPU on ESP32-C5 supports the Event Task Matrix (ETM) function, which allows LP CPU’s ETM tasks to be triggered by any peripherals’ ETM events, or LP CPU’s ETM events to trigger any peripherals’ ETM tasks.
This section introduces the ETM tasks and events related to the LP CPU. For more information, please refer to Chapter 12 Event Task Matrix (ETM).

LP CPU can receive the following ETM task:
```