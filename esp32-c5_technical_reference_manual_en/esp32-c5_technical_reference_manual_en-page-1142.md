

```markdown
- `0x06 (En_QPI)`: GP-SPI2 enters QPI mode when receiving this command and the bit `SPI_QPI_MODE` in register `SPI_USER_REG` is set.
- `0xDD (Ex_QPI)`: GP-SPI2 exits QPI mode when receiving this command and the bit `SPI_QPI_MODE` is cleared.

All the CMD values supported by GP-SPI2 are listed in Table 33.5-13 and Table 33.5-14. Note that the DUMMY state is always in 1-bit mode and lasts for eight SPI_CLK cycles.
```

Table 33.5-13. CMD Values Supported in SPI Mode

| Transfer Type | CMD[7:0] | CMD State   | ADDR State | DATA State |
|---------------|----------|-------------|------------|------------|
| Wr_BUF        | 0x01     | 1-bit mode  | 1-bit mode | 1-bit mode |
|               | 0x11     | 1-bit mode  | 1-bit mode | 2-bit mode |
|               | 0x21     | 1-bit mode  | 1-bit mode | 4-bit mode |
|               | 0x51     | 1-bit mode  | 2-bit mode | 2-bit mode |
|               | 0xA1     | 1-bit mode  | 4-bit mode | 4-bit mode |
|               | 0x02     | 1-bit mode  | 1-bit mode | 1-bit mode |
|               | 0x12     | 1-bit mode  | 1-bit mode | 2-bit mode |
|               | 0x22     | 1-bit mode  | 1-bit mode | 4-bit mode |
| Rd_BUF        | 0x52     | 1-bit mode  | 2-bit mode | 2-bit mode |
|               | 0xA2     | 1-bit mode  | 4-bit mode | 4-bit mode |
| Wr_DMA        | 0x03     | 1-bit mode  | 1-bit mode | 1-bit mode |
|               | 0x13     | 1-bit mode  | 1-bit mode | 2-bit mode |
|               | 0x23     | 1-bit mode  | 1-bit mode | 4-bit mode |
|               | 0x53     | 1-bit mode  | 2-bit mode | 2-bit mode |
|               | 0xA3     | 1-bit mode  | 4-bit mode | 4-bit mode |
| Rd_DMA        | 0x04     | 1-bit mode  | 1-bit mode | 1-bit mode |
|               | 0x14     | 1-bit mode  | 1-bit mode | 2-bit mode |
|               | 0x24     | 1-bit mode  | 1-bit mode | 4-bit mode |
|               | 0x54     | 1-bit mode  | 2-bit mode | 2-bit mode |
|               | 0xA4     | 1-bit mode  | 4-bit mode | 4-bit mode |
| CMD7          | 0x07     | 1-bit mode  | 1-bit mode | -          |
|               | 0x17     | 1-bit mode  | 1-bit mode | -          |
|               | 0x27     | 1-bit mode  | 1-bit mode | -          |
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
|               | 0x0A     | 1-bit mode  | 1-bit mode | -          |
```