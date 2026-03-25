

```markdown
- HP Peripherals
- LP Peripherals


Figure 6.3-1. System Structure and Address Mapping

Note:
* The range of addresses available in the address space may be larger than the actual available memory of a particular type.
* For CPU Sub-system, please refer to Chapter 2 High-Performance CPU.
* Some of the address space can only be accessed by the HP CPU, not by the LP CPU, as indicated in Figure 6.3-1. This part of the address space will not be specifically distinguished in the following sections.

Table 6.3-1 lists the address ranges on the data bus and instruction bus and their corresponding target memories.

Table 6.3-1. Memory Address Mapping

| Bus Type           | Boundary Address      |                     | Size   | Target         |
|--------------------|-----------------------|---------------------|--------|----------------|
|                    | Low Address           | High Address        |        |                |
|--------------------|-----------------------|---------------------|--------|----------------|
|                    | 0x0000_0000           | 0x3FFF_FFFF         | Reserved |                |
| Data/Instruction bus | 0x4000_0000           | 0x4004_FFFF         | 320 KB | ROM*           |
|                    | 0x4005_0000           | 0x407F_FFFF         | Reserved |                |
| Data/Instruction bus | 0x4080_0000           | 0x4085_FFFF         | 384 KB | HP SRAM*       |

Cont’d on next page
```