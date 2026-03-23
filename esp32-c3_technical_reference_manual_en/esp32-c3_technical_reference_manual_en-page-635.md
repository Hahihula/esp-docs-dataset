
```markdown
1/2/4-bit modes in states of CMD, ADDR, DATA are supported, which are determined by value of CMD[7:4].
The DUMMY state is always in 1-bit mode and lasts for eight SPI_CLK cycles. The definition of CMD[7:4] is as follows:

1. 0xO: CMD, ADDR, and DATA states all are in 1-bit mode.
2. 0x1: CMD and ADDR are in 1-bit mode. DATA is in 2-bit mode.
3. 0x2: CMD and ADDR are in 1-bit mode. DATA is in 4-bit mode.
4. 0x5: CMD is in 1-bit mode. ADDR and DATA are in 2-bit mode.
5. 0xA: CMD is in 1-bit mode, ADDR and DATA are in 4-bit mode. Or in QPI mode.

In addition, if the value of CMD[7:0] is 0xO5, 0xA5, 0xO6, or 0xDD, DUMMY and DATA states are omitted. The definition of CMD[7:0] is as follows:

1. 0xO5 (End_SEG_TRANS): master sends 0xO5 command to end slave segmented transfer in SPI mode.
2. 0xA5 (End_SEG_TRANS): master sends 0xA5 command to end slave segmented transfer in QPI mode.
3. 0xO6 (En_QPI): GP-SPI2 enters QPI mode when receiving the 0xO6 command and the bit `SPI_QPI_MODE` in register `SPI_USER_REG` is set.
4. 0xDD (Ex_QPI): GP-SPI2 exits QPI mode when receiving the 0xDD command and the bit `SPI_QPI_MODE` is cleared.

All the GP-SPI2 supported CMD values are listed in Table 27.5-11 and Table 27.5-12. Note that DUMMY state is always in 1-bit mode and lasts for eight SPI_CLK cycles.
```

```markdown
Table 27.5-11. Supported CMD Values in SPI Mode

| Transfer Type | CMD[7:0] | CMD State     | ADDR State    | DATA State     |
|---------------|----------|---------------|---------------|----------------|
|               |          | 1-bit mode    | 1-bit mode    | 1-bit mode     |
| Wr_BUF        | 0xO1     | 1-bit mode    | 1-bit mode    | 2-bit mode     |
|               | 0x11     | 1-bit mode    | 1-bit mode    | 4-bit mode     |
|               | 0x21     | 1-bit mode    | 1-bit mode    | 2-bit mode     |
|               | 0x51     | 1-bit mode    | 2-bit mode    | 4-bit mode     |
|               | 0xA1     | 1-bit mode    | 4-bit mode    | 1-bit mode     |
|               | 0xO2     | 1-bit mode    | 1-bit mode    | 2-bit mode     |
| Rd_BUF        | 0x12     | 1-bit mode    | 1-bit mode    | 4-bit mode     |
|               | 0x22     | 1-bit mode    | 2-bit mode    | 2-bit mode     |
|               | 0x52     | 1-bit mode    | 4-bit mode    | 4-bit mode     |
|               | 0xA2     | 1-bit mode    | 1-bit mode    | 2-bit mode     |
| Wr_DMA        | 0xO3     | 1-bit mode    | 1-bit mode    | 4-bit mode     |
|               | 0x13     | 1-bit mode    | 2-bit mode    | 4-bit mode     |
|               | 0x23     | 1-bit mode    | 4-bit mode    | 4-bit mode     |
|               | 0x53     | 1-bit mode    | 1-bit mode    | 2-bit mode     |
| Rd_DMA        | 0xO4     | 1-bit mode    | 1-bit mode    | 2-bit mode     |
|               | 0x14     | 1-bit mode    | 2-bit mode    | 4-bit mode     |
|               | 0x24     | 1-bit mode    | 4-bit mode    | 4-bit mode     |
|               | 0x54     | 1-bit mode    | 1-bit mode    | 2-bit mode     |
|               | 0xA4     | 1-bit mode    | 4-bit mode    | 4-bit mode     |
```