**Title:**
Chapter 20 SPI Controller (SPI)

**Header:**
Register 20.44. SPI_DMA_TSTATUS_REG (0x14C)

**Diagram/Block Diagram Description with Labels and Values:**
- RX_FIFO_EMPTY
- RX_FIFO_FULL
- (reserved)
- RX_DESC_ADDRESS

**Binary Representation Table:**
```
31 30 29 | ... ... ... ... ... ... ... ...
| Reset
0   0    0     O O       O O      O O      O O      O O      O O      O O      O O
```

**Descriptions of Register Bits:**
- RX_FIFO_EMPTY The SPI DMA RX FIFO is empty. (RO)
- RX_FIFO_FULL The SPI DMA RX FIFO is full. (RO)
- RX_DESC_ADDRESS The LSB of the SPI DMA inlink descriptor address. (RO)

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Page Number:**
ESP32 TRM (Version 5.6) - Page number not specified