
```markdown
| Bus Type                     | Boundary Address                 | Size   | Target         |
|------------------------------|-----------------------------------|--------|----------------|
|                              | Low Address High Address          |        |                |
| Data/Instruction bus         | 0x0000_0000 ~ 0x1FFF_FFFF         | 256 MB | CPU Sub-system |
|                              |                                   |        | Reserved       |
| Data/Instruction bus         | 0x3000_0000 ~ 0x3FFF_FFFF         | 128 KB | ROM*           |
|                              |                                   |        | Reserved       |
| Data/Instruction bus         | 0x4080_0000 ~ 0x41FF_FFFF         | 320 KB | HP SRAM*       |
|                              |                                   |        | Reserved       |
| Data/Instruction bus         | 0x4200_0000 ~ 0x42FF_FFFF         | 16 MB  | External memory|
|                              |                                   |        | Reserved       |
| Data/Instruction bus         | 0x5000_0000 ~ 0x5FFF_FFFF         | 4 KB   | LP SRAM*       |
|                              |                                   |        | Reserved       |
| Data/Instruction bus         | 0x6000_0000 ~ 0x600C_FFFF         | 832 KB | Peripherals    |
|                              | 0x600D_0000 ~ 0xFFFF_FFFF         |        | Reserved       |

\* All of the internal memories are managed by Permission Control module. An internal memory can only be accessed when it is allowed by Permission Control, then the internal memory can be available to CPU. For more information about Permission Control, please refer to Chapter 15 Permission Control (PMS).
```

## 4.3.2 Internal Memory

ESP32-H2 consists of the following three types of internal memory:

- ROM (128 KB): The ROM is a read-only memory and can not be programmed. It contains the ROM code of some low-level system software and read-only data.
- HP SRAM (320 KB): The HP SRAM is a volatile memory that can be quickly accessed by CPU (generally within a single clock cycle).
- LP SRAM (4 KB): LP SRAM is also a volatile memory, however, in Deep-sleep mode, data stored in the LP SRAM will not be lost. The LP SRAM can be accessed by CPU and is usually used to store program instructions and data that need to be kept in sleep mode.

### 1. ROM

This 128 KB ROM is a read-only memory, addressed by CPU through the instruction bus or through the data bus via `0x4000_0000 ~ 0x4001_FFFF`, as shown in Table 4.3-1.

### 2. HP SRAM

This 320 KB HP SRAM is a read-and-write memory, accessed by the CPU through the instruction bus or data bus as shown in Table 4.3-1.

### 3. LP SRAM
```