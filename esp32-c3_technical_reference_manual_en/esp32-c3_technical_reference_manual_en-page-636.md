

```markdown
| Transfer Type | CMD[7:0] | CMD State   | ADDR State | DATA State |
|---------------|----------|-------------|------------|------------|
| CMD7          | 0x07     | 1-bit mode  | 1-bit mode | -          |
|               | 0x17     | 1-bit mode  | 1-bit mode | -          |
|               | 0x27     | 1-bit mode  | 1-bit mode | -          |
| CMD8          | 0x57     | 1-bit mode  | 2-bit mode | -          |
|               | 0xA7     | 1-bit mode  | 4-bit mode | -          |
|               | 0x08     | 1-bit mode  | 1-bit mode | -          |
|               | 0x18     | 1-bit mode  | 1-bit mode | -          |
|               | 0x28     | 1-bit mode  | 1-bit mode | -          |
| CMD9          | 0x58     | 1-bit mode  | 2-bit mode | -          |
|               | 0xA8     | 1-bit mode  | 4-bit mode | -          |
|               | 0x09     | 1-bit mode  | 1-bit mode | -          |
|               | 0x19     | 1-bit mode  | 1-bit mode | -          |
| CMDA          | 0x29     | 1-bit mode  | 1-bit mode | -          |
|               | 0x59     | 1-bit mode  | 2-bit mode | -          |
|               | 0xA9     | 1-bit mode  | 4-bit mode | -          |
| End_SEG_TRAN  | 0x0A     | 1-bit mode  | 1-bit mode | -          |
| En_QPI         | 0x1A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x2A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x5A     | 1-bit mode  | 2-bit mode | -          |
|               | 0xAA     | 1-bit mode  | 4-bit mode | -          |
```

```markdown
| Transfer Type | CMD[7:0] | CMD State   | ADDR State | DATA State |
|---------------|----------|-------------|------------|------------|
| Wr_BUF        | 0xA1     | 4-bit mode  | 4-bit mode | 4-bit mode |
| Rd_BUF        | 0xA2     | 4-bit mode  | 4-bit mode | 4-bit mode |
| Wr_DMA        | 0xA3     | 4-bit mode  | 4-bit mode | 4-bit mode |
| Rd_DMA        | 0xA4     | 4-bit mode  | 4-bit mode | 4-bit mode |
| CMD7          | 0xA7     | 4-bit mode  | 4-bit mode | -          |
| CMD8          | 0xA8     | 4-bit mode  | 4-bit mode | -          |
| CMD9          | 0xA9     | 4-bit mode  | 4-bit mode | -          |
| CMDA          | 0xAA     | 4-bit mode  | 4-bit mode | -          |
| End_SEG_TRAN  | 0xA5     | 4-bit mode  | 4-bit mode | -          |
| Ex_QPI         | 0xDD     | 4-bit mode  | 4-bit mode | -          |
```

Master sends 0x06 CMD (En_QPI) to set GP-SPI2 slave to QPI mode and all the states of supported transfer will be in 4-bit mode afterwards. If 0xDD CMD (Ex_QPI) is received, GP-SPI2 slave will be back to SPI mode.

Other transfer types than described in Table 27.5-11 and Table 27.5-12 are ignored. If the transferred data is not in unit of byte, GP-SPI2 can send or receive these extra bits (total bits % 8), however, the correctness of the
```