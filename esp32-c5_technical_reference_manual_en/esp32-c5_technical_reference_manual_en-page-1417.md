

```markdown
Chapter 38 Controller Area Network Flexible Data-Rate (CAN FD)

Register 38.19. TWAIFD_RX_MEM_INFO_REG (0x0060)
| 31 | 29 | 28             | TWAIFD_RX_FREE | 16 | 15 | 13 | (reserved) | TWAIFD_RX_BUF_SIZE | 0 |
|----:|----:|----------------|---------------|----:|----:|----:|-----------:|--------------------|---|
|    0|    0|               Ox80|               |    0|    0|    0|           |                    |Reset|

TWAIFD_RX_BUF_SIZE Represents the size of the RX buffer in 32-bit words. (RO)
TWAIFD_RX_FREE Represents the number of free 32-bit words in the RX buffer. (RO)

Register 38.20. TWAIFD_RX_POINTERS_REG (0x0064)
| 31 | 28 | 27             | TWAIFD_RX_RPP | 16 | 15 | 12 | (reserved) | TWAIFD_RX_WPP | 0 |
|----:|----:|----------------|--------------|----:|----:|----:|-----------:|--------------|---|
|    0|    0|               0x0|              |    0|    0|    0|           |              |Reset|

TWAIFD_RX_WPP Represents the write pointer position in the RX buffer. The pointer is updated upon storing a received frame. (RO)
TWAIFD_RX_RPP Represents the read pointer position in the RX buffer. The pointer is updated upon reading a received frame. (RO)
```