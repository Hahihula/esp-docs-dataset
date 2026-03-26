

```markdown
Chapter 8 eFuse Controller (EFUSE)
GoBack

Register 8.13. EFUSE_RD_MAC_SYS4_REG (0x0054)

![Diagram for EFUSE_SYS_DATA_PARTO_1](#)  
`EFUSE_SYS_DATA_PARTO_1`  

| 31 | 0 |
|----|---|
|    | Reset |
| 0x000000 |          |

EFUSE_SYS_DATA_PARTO_1 Represents the first 32 bits of the zeroth part of system data. (RO)

Register 8.14. EFUSE_RD_MAC_SYS5_REG (0x0058)

![Diagram for EFUSE_SYS_DATA_PARTO_2](#)  
`EFUSE_SYS_DATA_PARTO_2`  

| 31 | 0 |
|----|---|
|    | Reset |
| 0x000000 |          |

EFUSE_SYS_DATA_PARTO_2 Represents the second 32 bits of the zeroth part of system data. (RO)

Register 8.15. EFUSE_RD_SYS_PART1_DATA_n_REG (n: 0-7) (0x005C+0x4*n)

![Diagram for EFUSE_SYS_DATA_PART1_n](#)  
`EFUSE_SYS_DATA_PART1_n`  

| 31 | 0 |
|----|---|
|    | Reset |
| 0x000000 |          |

EFUSE_SYS_DATA_PART1_n Represents the nth 32 bits of the first part of system data. (RO)
```