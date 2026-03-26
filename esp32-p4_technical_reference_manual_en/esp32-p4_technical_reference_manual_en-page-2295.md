

```markdown
## 43.13.2 GP-SPI3 Register

The addresses in this section are relative to GP-SPI3 base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 43.39. SPI_CMD_REG (0x0000)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 25  |                     |
| 24  |                     |
| 23  |                     |
| 22  |                     |
|     | SPI_USR             |
|     | SPI_UPDATE          |
| ... |                     |
| 0   | Reset               |

**SPI_UPDATE**: Configures whether or not to synchronize SPI registers from APB clock domain into SPI module clock domain.

- 0: Not synchronize
- 1: Synchronize

This bit is only used in SPI master transfer. (WT)

**SPI_USR**: Configures whether or not to enable user-defined command.

- 0: Not enable
- 1: Enable

An SPI operation will be triggered when the bit is set. This bit will be cleared once the operation is done. (R/W/SC)

### Register 43.40. SPI_ADDR_REG (0x0004)

| Bit | Description         |
|-----|---------------------|
| 31  |                     |
| ... |                     |
| 0   | Reset               |

**SPI_USR_ADDR_VALUE**: Configures the address to slave. (R/W)
```