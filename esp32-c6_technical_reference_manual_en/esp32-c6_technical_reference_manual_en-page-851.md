

```markdown
Table 28.5-13. Supported CMD Values in SPI Mode

| Transfer Type | CMD[7:0] | CMD State   | ADDR State | DATA State |
|---------------|----------|-------------|------------|------------|
|               | 0xA9     | 1-bit mode  | 4-bit mode | -          |
|               | 0xOA     | 1-bit mode  | 1-bit mode | -          |
| CM DA         | 0x1A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x2A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x5A     | 1-bit mode  | 2-bit mode | -          |
|               | 0xAA     | 1-bit mode  | 4-bit mode | -          |
| End_SEG_TRAN  | 0x05     | 1-bit mode  | -          | -          |
| En_QPI         | 0x06     | 1-bit mode  | -          | -          |

Table 28.5-14. Supported CMD Values in QPI Mode

| Transfer Type | CMD[7:0] | CMD State   | ADDR State | DATA State |
|---------------|----------|-------------|------------|------------|
| Wr_BUF        | 0xA1     | 4-bit mode  | 4-bit mode | 4-bit mode |
| Rd_BUF        | 0xA2     | 4-bit mode  | 4-bit mode | 4-bit mode |
| Wr_DMA        | 0xA3     | 4-bit mode  | 4-bit mode | 4-bit mode |
| Rd_DMA        | 0xA4     | 4-bit mode  | 4-bit mode | 4-bit mode |
| CMD7          | 0xA7     | 4-bit mode  | 4-bit mode | -          |
| CMD8          | 0xA8     | 4-bit mode  | 4-bit mode | -          |
| CMD9          | 0xA9     | 4-bit mode  | 4-bit mode | -          |
| CM DA         | 0xAA     | 4-bit mode  | 4-bit mode | -          |
| End_SEG_TRAN  | 0xA5     | 4-bit mode  | 4-bit mode | -          |
| Ex_QPI         | 0xDD     | 4-bit mode  | 4-bit mode | -          |

Master sends 0x06 CMD (En_QPI) to set GP-SPI2 slave to QPI mode and all the states of supported transfer will be in 4-bit mode afterwards. If 0xDD CMD (Ex_QPI) is received, GP-SPI2 slave will be back to SPI mode.

Other transfer types than these described in Table 28.5-13 and Table 28.5-14 are ignored. If the transferred data is not in unit of byte, GP-SPI2 will send or receive the data in unit of byte, but the extra bits (the result of total bits mod 8) will be lost. But if the CS low time is longer than 2 APB clock (APB_CLK) cycles, SPI_TRANS_DONE_INT will be triggered. For more information on interrupts triggered at the end of transmissions, please refer to Section 28.9.

28.5.9.3 Slave Single Transfer and Slave Segmented Transfer

When GP-SPI2 works as a slave, it supports full-duplex and half-duplex communications controlled by DMA and by CPU. DMA-controlled transfer can be a single transfer, or a slave segmented transfer consisting of several transactions (segments). The CPU-controlled transfer can only be one single transfer, since each CPU-controlled transaction needs to be triggered by CPU.

In a slave segmented transfer, all transfer types listed in Table 28.5-13 and Table 28.5-14 are supported in a single transaction (segment). It means that CPU-controlled transaction and DMA-controlled transaction can be mixed in one slave segmented transfer.

It is recommended that in a slave segmented transfer:
```