

```markdown
Chapter 4 System and Memory

GoBack

CPU
0x0000_0000
0x1FFF_FFFF
0x2000_0000
0x2FFF_FFFF
0x3000_0000
0x3FFF_FFFF
0x4000_0000
0x4001_FFFF
0x4002_0000
0x407F_FFFF
0x4080_0000
0x4084_FFFF
0x4085_0000
0x41FF_FFFF
0x4200_0000
0x42FF_FFFF
0x4300_0000
0x4FFF_FFFF
0x5000_0000
0x5000_0FFF
0x5000_1000
0x5FFF_FFFF
0x6000_0000
0x600C_FFFF
0x600D_0000
0xFFFF_FFFF

CPU Sub-system
ROM (128 KB)
HP Memory (320 KB)
GDMA
LP Memory (4 KB)
Peripherals

Cache
MMU
External Memory

Not available for use

Figure 4.2-1. System Structure and Address Mapping

Note:
* The range of addresses available in the address space may be larger than the actual available memory of a particular type.
* For CPU Sub-system, please refer to Chapter 1 ESP-RISC-V CPU.

4.3 Functional Description

4.3.1 Address Mapping

All the non-reserved addresses are accessible by the instruction bus and data bus, that is, the instruction bus and the data bus access the same address space.

Both data bus and instruction bus of CPU are little-endian.

CPU can access data via the data bus using single-byte, double-byte, and 4-byte alignment.

The CPU can:
* directly access the internal memory via both data bus and instruction bus.
* directly access the external memory which is mapped into the address space via cache.

Espressif Systems
143
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```