

```markdown
| Transfer Type | CMD[7:0] | CMD State   | ADDR State | DATA State |
|---------------|----------|-------------|------------|------------|
| Rd_DMA        | 0xA3     | 1-bit mode  | 4-bit mode | 4-bit mode |
|               | 0x04     | 1-bit mode  | 1-bit mode | 1-bit mode |
|               | 0x14     | 1-bit mode  | 1-bit mode | 2-bit mode |
|               | 0x24     | 1-bit mode  | 1-bit mode | 4-bit mode |
|               | 0x54     | 1-bit mode  | 2-bit mode | 2-bit mode |
|               | 0xA4     | 1-bit mode  | 4-bit mode | 4-bit mode |
|               | 0x07     | 1-bit mode  | 1-bit mode | -          |
|               | 0x17     | 1-bit mode  | 1-bit mode | -          |
| CMD7          | 0x27     | 1-bit mode  | 1-bit mode | -          |
|               | 0x57     | 1-bit mode  | 2-bit mode | -          |
|               | 0xA7     | 1-bit mode  | 4-bit mode | -          |
| CMD8          | 0x08     | 1-bit mode  | 1-bit mode | -          |
|               | 0x18     | 1-bit mode  | 1-bit mode | -          |
|               | 0x28     | 1-bit mode  | 1-bit mode | -          |
|               | 0x58     | 1-bit mode  | 2-bit mode | -          |
|               | 0xA8     | 1-bit mode  | 4-bit mode | -          |
| CMD9          | 0x09     | 1-bit mode  | 1-bit mode | -          |
|               | 0x19     | 1-bit mode  | 1-bit mode | -          |
|               | 0x29     | 1-bit mode  | 1-bit mode | -          |
|               | 0x59     | 1-bit mode  | 2-bit mode | -          |
|               | 0xA9     | 1-bit mode  | 4-bit mode | -          |
| CMDA          | 0x0A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x1A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x2A     | 1-bit mode  | 1-bit mode | -          |
|               | 0x5A     | 1-bit mode  | 2-bit mode | -          |
|               | 0xAA     | 1-bit mode  | 4-bit mode | -          |
| End_SEG_TRANS | 0x05     | 1-bit mode  | -          | -          |
| En_QPI        | 0x06     | 1-bit mode  | -          | -          |

Table 43.5-17. CMD Values Supported in QPI Mode

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
| End_SEG_TRANS | 0xA5     | 4-bit mode  | 4-bit mode | -          |
| Ex_QPI        | 0xDD     | 4-bit mode  | 4-bit mode | -          |
```