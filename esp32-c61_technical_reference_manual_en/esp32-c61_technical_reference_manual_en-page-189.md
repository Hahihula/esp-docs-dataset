

```markdown
## Register 3.30. AHB_DMA_DATE_REG (0x0068)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  |                    |                                                                             |
|     | `AHB_DMA_DATE`     | Version control register. (R/W)                                             |

### Register 3.31. AHB_DMA_INFIFO_STATUS_CHn_REG (n: 0-1) (0x0078+0xC0*n)

```markdown
| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | `(reserved)`                                |                                                                             |
| 28  | `AHB_DMA_IN_BUF_HUNGRY_CHn`                | (RO)                                                                         |
| 27  | `AHB_DMA_IN_REMAIN_UNDER_4B_CHn`           | Reserved. (RO)                                                               |
| 26  | `AHB_DMA_IN_REMAIN_UNDER_3B_CHn`           | Reserved. (RO)                                                               |
| 25  | `AHB_DMA_IN_REMAIN_UNDER_2B_CHn`           | Reserved. (RO)                                                               |
| 24  | `AHB_DMA_IN_REMAIN_UNDER_1B_CHn`           | Reserved. (RO)                                                               |
| 23  | `(reserved)`                                |                                                                             |
| 22  | `AHB_DMA_INFIFO_FULL_CHn`                  | Represents whether L1 RX FIFO is full.<br>O: Not Full<br>1: Full (RO)        |
| 21  | `AHB_DMA_INFIFO_EMPTY_CHn`                 | Represents whether L1 RX FIFO is empty.<br>O: Not empty<br>1: Empty (RO)     |
| 20  | `AHB_DMA_INFIFO_CNT_CHn`                   | Represents the number of data bytes in L1 RX FIFO for RX channel n. (RO)    |
| 15  | `(reserved)`                                |                                                                             |
| 8   | `AHB_DMA_IN_REMAIN_UNDER_4B_CHn`           | Reserved. (RO)                                                               |
| 7   | `AHB_DMA_IN_REMAIN_UNDER_3B_CHn`           | Reserved. (RO)                                                               |
| 6   | `AHB_DMA_IN_REMAIN_UNDER_2B_CHn`           | Reserved. (RO)                                                               |
| 5   | `AHB_DMA_IN_REMAIN_UNDER_1B_CHn`           | Reserved. (RO)                                                               |
| 4   | `(reserved)`                                |                                                                             |
| 3   | `AHB_DMA_INFIFO_FULL_CHn`                  | Represents whether L1 RX FIFO is full.<br>O: Not Full<br>1: Full (RO)        |
| 2   | `AHB_DMA_INFIFO_EMPTY_CHn`                 | Represents whether L1 RX FIFO is empty.<br>O: Not empty<br>1: Empty (RO)     |
| 1   | `(reserved)`                                |                                                                             |
| 0   | Reset                                       | 1                                                                             |

```
```markdown
AHB_DMA_INFIFO_FULL_CHn Represents whether L1 RX FIFO is full.
O: Not Full
1: Full (RO)

AHB_DMA_INFIFO_EMPTY_CHn Represents whether L1 RX FIFO is empty.
O: Not empty
1: Empty (RO)

AHB_DMA_INFIFO_CNT_CHn Represents the number of data bytes in L1 RX FIFO for RX channel n. (RO)

AHB_DMA_IN_REMAIN_UNDER_1B_CHn Reserved. (RO)
AHB_DMA_IN_REMAIN_UNDER_2B_CHn Reserved. (RO)
AHB_DMA_IN_REMAIN_UNDER_3B_CHn Reserved. (RO)
AHB_DMA_IN_REMAIN_UNDER_4B_CHn Reserved. (RO)
AHB_DMA_IN_BUF_HUNGRY_CHn Reserved. (RO)
```