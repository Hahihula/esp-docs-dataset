
```markdown
| Bus Type | Boundary Address Low Address | High Address | Size   | Target         |
|----------|------------------------------|--------------|--------|----------------|
|          | 0x0000_0000                  | 0x3FFF_FFFF  |        | Reserved       |
| Data/Instruction bus | 0x4000_0000                  | 0x4004_FFFF  | 320 KB | ROM*           |
|          | 0x4005_0000                  | 0x407F_FFFF  |        | Reserved       |
| Data/Instruction bus | 0x4080_0000                  | 0x4087_FFFF  | 512 KB | HP SRAM*       |
|          | 0x4088_0000                  | 0x41FF_FFFF  |        | Reserved       |
| Data/Instruction bus | 0x4200_0000                  | 0x42FF_FFFF  | 16 MB  | External memory|
|          | 0x4300_0000                  | 0x4FFF_FFFF  |        | Reserved       |
| Data/Instruction bus | 0x5000_0000                  | 0x5000_3FFF  | 16 KB  | LP SRAM*       |
|          | 0x5000_4000                  | 0x5FFF_FFFF  |        | Reserved       |
| Data/Instruction bus | 0x6000_0000                  | 0x600C_FFFF  | 832 KB | Peripherals    |
|          | 0x600D_0000                  | 0xFFFF_FFFF  |        | Reserved       |

* All of the internal memories are managed by Permission Control module. An internal memory can only be accessed when it is allowed by Permission Control, then the internal memory can be available to the HP CPU and LP CPU. For more information about Permission Control, please refer to Chapter 16 Permission Control (PMS).
```

## 5.3.2 Internal Memory

ESP32-C6 consists of the following three types of internal memory:

- ROM (320 KB): The ROM is a read-only memory and can not be programmed. It contains the ROM code of some low-level system software and read-only data.
- HP SRAM (512 KB): The HP SRAM is a volatile memory that can be quickly accessed by the HP CPU or LP CPU (generally within a single HP CPU clock cycle for HP CPU).
- LP SRAM (16 KB): LP SRAM is also a volatile memory, however, in Deep-sleep mode, data stored in the LP SRAM will not be lost. The LP SRAM can be accessed by the HP CPU or LP CPU and is usually used to store program instructions and data that need to be kept in sleep mode.

### 1. ROM

This 320 KB ROM is a read-only memory, addressed by the HP CPU through the instruction bus or through the data bus via `0x4000_0000 ~ 0x4004_FFFF`, as shown in Table 5.3-1.

### 2. HP SRAM

This 512 KB HP SRAM is a read-and-write memory, accessed by the HP CPU or LP CPU through the instruction bus or through the data bus as shown in Table 5.3-1.

### 3. LP SRAM

This 16 KB LP SRAM is a read-and-write memory, accessed by the HP CPU or LP CPU through the instruction bus or through the data bus via their shared address `0x5000_0000 ~ 0x5000_3FFF` as shown in Table 5.3-1.
```