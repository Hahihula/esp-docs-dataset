

```markdown
Chapter 37 Remote Control Peripheral (RMT)
GoBack

37.5 Registers

The addresses in this section are relative to Remote Control Peripheral base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 371. RMT_CHnDATA_REG (n: 0-3) (0x0000+0x4*n)

RMT_CHnDATA

| 31 | 0 |
|----|---|
| 0x000000 | Reset |

RMT_CHnDATA Read and write data for channel n via APB FIFO. (HRO)
```