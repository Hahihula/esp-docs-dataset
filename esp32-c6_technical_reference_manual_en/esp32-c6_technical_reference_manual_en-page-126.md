

```markdown
| Counter          | Counted Event                                                                 |
|------------------|-------------------------------------------------------------------------------|
| mhpcounter4      | Wait cycles for fetching instructions                                        |
| mhpcounter5      | The number of memory read operations. An unaligned read is counted as two.    |
| mhpcounter6      | The number of memory write operations. An unaligned write is counted as two.  |
| mhpcounter7      | The number of unconditional jump instructions (jal, jr, jalr)                 |
| mhpcounter8      | The number of branch instructions                                             |
| mhpcounter9      | The number of taken branch instructions                                       |
| mhpcounter10     | The number of compressed instructions                                        |
| mhpcounter11     | Wait cycles for multiplication instructions                                   |
| mhpcounter12     | Wait cycles for division instructions                                        |

## 3.7 System Access

### 3.7.1 Memory Access

The ESP32-C6 LP CPU can access LP SRAM and HP SRAM. For more information, please refer to Section 5 System and Memory.

*   LP SRAM: 16 KB starting from 0x5000_0000 to 0x5000_3FFF, where you can fetch instructions, read data, write data, etc.
*   HP SRAM: 512 KB starting from 0x4080_0000 to 0x4087_FFFF, where you can fetch instructions, read data, write data, etc.

**Note:**  
The LP CPU has a high latency to access the HP SRAM, but can access the LP SRAM with no latency.

The LP CPU supports the atomic instruction set. Both the LP CPU and the HP CPU can access memory through atomic instructions, thus achieving atomicity of memory access. For details on the atomic instruction set, please refer to RISC-V Instruction Set Manual Volume I: Unprivileged ISA, Version 2.2.

### 3.7.2 Peripheral Access

Table 5.3-2 in Chapter 5 System and Memory lists the peripherals accessible by the LP CPU and their base addresses.

## 3.8 Event Task Matrix Feature

The LP CPU on ESP32-C6 supports the Event Task Matrix (ETM) function, which allows LP CPU’s ETM tasks to be triggered by any peripherals’ ETM events, or LP CPU’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to the LP CPU. For more information, please refer to Chapter 11 Event Task Matrix (SOC_ETM).

LP CPU can receive the following ETM task:

*   ULP_TASK_WAKEUP_CPU: Wakes up the LP CPU.
```