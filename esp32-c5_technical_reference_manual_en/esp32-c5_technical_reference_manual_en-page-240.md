

```markdown
| Bus Type               | Boundary Address          | Size   | Target         |
|------------------------|----------------------------|--------|----------------|
|                        | Low Address               | High Address |        |
| Data/Instruction bus  | 0x4086_0000                | 0x41FF_FFFF    | Reserved      |
| Data/Instruction bus  | 0x4200_0000                | 0x43FF_FFFF    | 32 MB External memory |
|                        | 0x4400_0000                | 0x4FFF_FFFF    | Reserved      |
| Data/Instruction bus  | 0x5000_0000                | 0x5000_3FFF    | 16 KB LP SRAM* |
|                        | 0x5000_4000                | 0x5FFF_FFFF    | Reserved      |
| Data/Instruction bus  | 0x6000_0000                | 0x600C_FFFF    | 832 KB Peripherals |
|                        | 0x600D_0000                | 0xFFFF_FFFF    | Reserved      |

* All of the internal memories are managed by Permission Control module. An internal memory can only be accessed when it is allowed by Permission Control, then the internal memory can be available to the HP CPU and LP CPU. For more information about Permission Control, please refer to Chapter 18 Permission Control (PMS).
```

## 6.3.2 Internal Memory

ESP32-C5 has various types of internal memory:

* ROM (320 KB): The ROM is a read-only memory and can not be programmable. It contains the ROM code of some low-level system software and read-only data. Note that this memory can only be accessed by HP CPU.
* HP SRAM (384 KB): The HP SRAM is a volatile memory that can be quickly accessed by the HP CPU or LP CPU (generally within a single HP CPU clock cycle for HP CPU).
* LP SRAM (16 KB): The LP SRAM is also a volatile memory, however, in Deep-sleep mode, data stored in the LP SRAM will not be lost. The LP SRAM can be accessed by the HP CPU or LP CPU and is usually used to store program instructions and data that need to be kept in sleep mode.

### 6.3.2.1 ROM

This 320 KB ROM is a read-only memory, accessed by the HP CPU directly through the instruction bus or through the data bus via 0x4000_0000 ~ 0x4004_FFFF or via ROM-Cache, see Table 6.3-1.

As shown in Figure 6.3-2, ESP32-C5 is able to access ROM via ROM-Cache. This 4 KB ROM-Cache is two-way set associative, with a block size of 64 bytes. Both the instruction bus and the data bus can access the ROM-Cache at the same time, and the ROM-Cache responds to one or the other through arbitration. If data missing happens, ROM-Cache controller initiates a request to the ROM.
```