
```markdown
Register 14.76. SYSCON_FLASH_ACEN_SIZE_REG (n: 0-3) (0x0048 + 4*n)

| Bit Range | Description         |
|-----------|---------------------|
| 31        | (reserved)          |
| 16-15     |                     |
| 0-0       | SYSCON_FLASH_ACEN_SIZE |
|           | Reset               |

SYSCON_FLASH_ACEN_SIZE Configure the length of Flash Region n. The size of each region should be aligned to 64 KB. (R/W)

Register 14.77. SYSCON_SPI_MEM_PMS_CTRL_REG (0x0088)

| Bit Range | Description                                |
|-----------|--------------------------------------------|
| 31        | (reserved)                                 |
| 7-6       | SYSCON_SPI_MEM_REJECT_CLR                  |
| 2-1       | SYSCON_SPI_MEM_REJECT_INT                  |
| 0-0       | SYSCON_SPI_MEM_REJECT_CDE                  |
|           | Reset                                      |

SYSCON_SPI_MEM_REJECT_INT Indicates exception accessing external memory and triggers an interrupt. (RO)

SYSCON_SPI_MEM_REJECT_CLR Set this bit to clear the exception status. (WT)

SYSCON_SPI_MEM_REJECT_CDE Stores the exception cause: invalid region, overlapping regions, illegal write, illegal read and illegal instruction execution. (RO)
```