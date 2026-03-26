

```markdown
Register 43.77. LP_SPI_CMD_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31  | Reset       |
|     |             |
| 25  | (reserved)  |
| 24  | LP_SPI_USR   |
| 23  | LP_SPI_UPDATE|

LP_SPI_UPDATE Configures whether or not to synchronize SPI registers from APB clock domain into SPI module clock domain.
0: Not synchronize
1: Synchronize
This bit is only used in SPI master transfer.
(WT)

LP_SPI_USR Configures whether or not to enable user-defined command.
0: Not enable
1: Enable
An SPI operation will be triggered when the bit is set. This bit will be cleared once the operation is done.
(R/W/SC)
```

```markdown
Register 43.78. LP_SPI_ADDR_REG (0x0004)

| Bit | Description |
|-----|-------------|
| 31  | Reset       |
|     |             |
| 0   | LP_SPI_USR_ADDR_VALUE|

LP_SPI_USR_ADDR_VALUE Configures the address to slave.
(R/W)
```