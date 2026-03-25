

```markdown
Chapter 4 System and Memory                                                                 GoBack


Figure 4.3-1. System Structure and Address Mapping



Note:
1. The range of addresses available in the address space may be larger than the actual available memory of a particular type.
2. Part of the internal memory is reserved for system instructions and data, therefore, the address range available in the address space may be larger than the actual available internal memory.
3. For CPU Sub-system, please refer to Chapter 1 ESP-RISC-V CPU.



Table 4.3-1 lists the address ranges on the data bus and instruction bus and their corresponding target memories.


Table 4.3-1. Memory Address Mapping
| Bus Type          | Boundary Address | Size   | Target |
|-------------------|-------------------|--------|--------|
|                   | Low Address       | High Address |        |        |
|                   | 0x0000_0000       | 0x3FFF_FFFF    |        | Reserved |
| Data/Instruction bus | 0x4000_0000      | 0x4003_FFFF    | 256 KB | ROM*   |

Cont'd on next page
```