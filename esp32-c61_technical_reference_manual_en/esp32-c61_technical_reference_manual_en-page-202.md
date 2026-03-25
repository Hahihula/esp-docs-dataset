

```markdown
| Bus Type               | Boundary Address          | Size   | Target         |
|------------------------|----------------------------|--------|----------------|
|                        | Low Address               | High Address |        |
| Data/Instruction bus   | 0x4004_0000                | 0x407F_FFFF    | Reserved      |
|                        | 0x4080_0000                | 0x4084_FFFF    | 320 KB        | HP SRAM*     |
|                        | 0x4085_0000                | 0x41FF_FFFF    | Reserved      |
| Data/Instruction bus   | 0x4200_0000                | 0x43FF_FFFF    | 32 MB         | External memory |
|                        | 0x4400_0000                | 0x5FFFF_FFFF    | Reserved      |
| Data bus               | 0x6000_0000                | 0x600C_FFFF    | 832 KB        | Peripherals   |
|                        | 0x600D_0000                | 0xFFFF_FFFF    | Reserved      |

* All of the internal memories are managed by Permission Control module. An internal memory can only be accessed when it is allowed by Permission Control, then the internal memory can be available to the CPU. For more information about Permission Control, please refer to Chapter 16 Permission Control (PMS).
```

## 4.3.2 Internal Memory

ESP32-C61 has various types of internal memory:

* ROM (256 KB): The ROM is a read-only memory and can not be programmable. It contains the ROM code of some low-level system software and read-only data. Note that this memory can only be accessed by CPU.
* HP SRAM (320 KB): The HP SRAM is a volatile memory that can be quickly accessed by the CPU (generally within a single CPU clock cycle).

### 4.3.2.1 ROM

This 256 KB ROM is a read-only memory, accessed by the CPU directly through the instruction bus or through the data bus via the address range (0x4000_0000~0x4003_FFFF), see Table 4.3-1.

### 4.3.2.2 HP SRAM

This 320 KB HP SRAM is a read-and-write memory, accessed by the CPU through the instruction bus or data bus via the address range (0x4080_0000~0x4084_FFFF), see Table 4.3-1.

## 4.3.3 External Memory

ESP32-C61 supports SPI, Dual SPI, Quad SPI, and QPI interfaces that allow connection to external flash and RAM. ESP32-C61 also supports hardware manual encryption and automatic encryption/decryption based on XTS-AES algorithm to protect users’ programs and data in the external flash and RAM.

### 4.3.3.1 External Memory Address Mapping

The external memory can be accessed by CPU via the cache or accessed by the GDMA. According to the information inside the MMU (Memory Management Unit), the cache maps the CPU and GDMA’s address (0x4200_0000~0x43FF_FFFF) into a physical address of the external memory. With this address mapping, ESP32-C61 can address up to 32 MB external flash and 32 MB external RAM.
```