

```markdown
| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Timing registers                     |                                                                             |           |        |
| SPI_DIN_MODE_REG                     | SPI input delay mode configuration                                         | 0x0024    | varies |
| SPI_DIN_NUM_REG                      | SPI input delay number configuration                                       | 0x0028    | varies |
| SPI_DOUT_MODE_REG                    | SPI output delay mode configuration                                        | 0x002C    | varies |
| Interrupt registers                  |                                                                             |           |        |
| SPI_DMA_INT_ENA_REG                  | SPI interrupt enable register                                               | 0x0034    | R/W    |
| SPI_DMA_INT_CLR_REG                  | SPI interrupt clear register                                                | 0x0038    | WT     |
| SPI_DMA_INT_RAW_REG                  | SPI interrupt raw register                                                  | 0x003C    | R/WTC/SS|
| SPI_DMA_INT_ST_REG                   | SPI interrupt status register                                               | 0x0040    | RO     |
| SPI_DMA_INT_SET_REG                  | SPI interrupt software set register                                        | 0x0044    | WT     |
| CPU-controlled data buffer           |                                                                             |           |        |
| SPI_WO_REG                           | SPI CPU-controlled buffer0                                                 | 0x0098    | R/W/SS |
| SPI_W1_REG                           | SPI CPU-controlled buffer1                                                 | 0x009C    | R/W/SS |
| SPI_W2_REG                           | SPI CPU-controlled buffer2                                                 | 0x00AO    | R/W/SS |
| SPI_W3_REG                           | SPI CPU-controlled buffer3                                                 | 0x00A4    | R/W/SS |
| SPI_W4_REG                           | SPI CPU-controlled buffer4                                                 | 0x00A8    | R/W/SS |
| SPI_W5_REG                           | SPI CPU-controlled buffer5                                                 | 0x00AC    | R/W/SS |
| SPI_W6_REG                           | SPI CPU-controlled buffer6                                                 | 0x00BO    | R/W/SS |
| SPI_W7_REG                           | SPI CPU-controlled buffer7                                                 | 0x00B4    | R/W/SS |
| SPI_W8_REG                           | SPI CPU-controlled buffer8                                                 | 0x00B8    | R/W/SS |
| SPI_W9_REG                           | SPI CPU-controlled buffer9                                                 | 0x00BC    | R/W/SS |
| SPI_W10_REG                          | SPI CPU-controlled buffer10                                                | 0x00CO    | R/W/SS |
| SPI_W11_REG                          | SPI CPU-controlled buffer11                                                | 0x00C4    | R/W/SS |
| SPI_W12_REG                          | SPI CPU-controlled buffer12                                                | 0x00C8    | R/W/SS |
| SPI_W13_REG                          | SPI CPU-controlled buffer13                                                | 0x00CC    | R/W/SS |
| SPI_W14_REG                          | SPI CPU-controlled buffer14                                                | 0x00DO    | R/W/SS |
| SPI_W15_REG                          | SPI CPU-controlled buffer15                                                | 0x00D4    | R/W/SS |
| Version register                     |                                                                             |           |        |
| SPI_DATE_REG                         | Version control                                                             | 0x00FO    | R/W    |

## 28.11 Registers

The addresses in this section are relative to SPI base address provided in Table 5.3-2 in Chapter 5 System and Memory.
```