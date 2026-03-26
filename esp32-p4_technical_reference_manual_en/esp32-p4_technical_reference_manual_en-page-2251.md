
```markdown
| Name               | Description          | Address   | Access |
|--------------------|----------------------|-----------|--------|
| SPI_DATE_REG       | Version control      | 0x00FO    | R/W    |

## 43.12.2 GP-SPI3 Register Summary

The addresses in this section are relative to GP-SPI3 base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                               | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------|-----------|--------|
| **User-defined control registers**         |                                                           |           |        |
| SPI_CMD_REG                               | Command control register                                  | 0x0000    | varies |
| SPI_ADDR_REG                              | Address value register                                    | 0x0004    | R/W    |
| SPI_USER_REG                              | SPI USER control register                                 | 0x0010    | varies |
| SPI_USER1_REG                             | SPI USER control register 1                               | 0x0014    | R/W    |
| SPI_USER2_REG                             | SPI USER control register 2                               | 0x0018    | R/W    |
| **Control and configuration registers**    |                                                           |           |        |
| SPI_CTRL_REG                              | SPI control register                                      | 0x0008    | R/W    |
| SPI_MS_DLEN_REG                           | SPI data bit length control register                      | 0x001C    | R/W    |
| SPI_MISC_REG                              | SPI misc register                                         | 0x0020    | R/W    |
| SPI_DMA_CONF_REG                          | SPI DMA control register                                  | 0x0030    | varies |
| SPI_SLAVE_REG                             | SPI slave control register                                | 0x00EO    | varies |
| SPI_SLAVE1_REG                            | SPI slave control register 1                              | 0x00E4    | R/W/SS |
| **Clock control registers**               |                                                           |           |        |
| SPI_CLOCK_REG                             | SPI clock control register                                | 0x00OC    | R/W    |
| SPI_CLK_GATE_REG                          | SPI module clock and register clock control               | 0x00E8    | R/W    |
| **Timing registers**                      |                                                           |           |        |
| SPI_DIN_MODE_REG                          | SPI input delay mode configuration                        | 0x0024    | R/W    |
| SPI_DIN_NUM_REG                           | SPI input delay number configuration                      | 0x0028    | R/W    |
| SPI_DOUT_MODE_REG                         | SPI output delay mode configuration                       | 0x002C    | R/W    |
| **Interrupt registers**                   |                                                           |           |        |
| SPI_DMA_INT_ENA_REG                       | SPI interrupt enable register                             | 0x0034    | R/W    |
| SPI_DMA_INT_CLR_REG                       | SPI interrupt clear register                              | 0x0038    | WT     |
| SPI_DMA_INT_RAW_REG                       | SPI interrupt raw register                                | 0x003C    | R/WTC/SS|
| SPI_DMA_INT_ST_REG                        | SPI interrupt status register                             | 0x0040    | RO     |
| SPI_DMA_INT_SET_REG                       | SPI interrupt software set register                       | 0x0044    | WT     |
| **CPU-controlled data buffer**            |                                                           |           |        |
| SPI_WO_REG                                | SPI CPU-controlled buffer 0                               | 0x0098    | R/W/SS |
| SPI_W1_REG                                | SPI CPU-controlled buffer 1                               | 0x009C    | R/W/SS |
| SPI_W2_REG                                | SPI CPU-controlled buffer 2                               | 0x00AO    | R/W/SS |
| SPI_W3_REG                                | SPI CPU-controlled buffer 3                               | 0x00A4    | R/W/SS |
| SPI_W4_REG                                | SPI CPU-controlled buffer 4                               | 0x00A8    | R/W/SS |
| SPI_W5_REG                                | SPI CPU-controlled buffer 5                               | 0x00AC    | R/W/SS |
| SPI_W6_REG                                | SPI CPU-controlled buffer 6                               | 0x00BO    | R/W/SS |
```