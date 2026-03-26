

```markdown
Chapter 54 SD/MMC Host Controller (SDHOST)

- CKLENA - clock enable
- CLKSRC - clock source
- TMOUT - timeout
- CTYPE - card type

## 54.6 RAM for Receiving and Transmitting Data

The submodule RAM is a buffer area for transmitting and receiving data. It can be divided into two units: one is for transmitting data, and the other is for receiving data. The process of transmitting and receiving data can be achieved by the CPU and DMA for reading and writing. The latter method is described in detail in Section 54.8.

### 54.6.1 TX RAM Module

There are two ways to enable a write operation: CPU and DMA write.

For CPU write operations to TX RAM, write the data directly into the SDHOST_BUFFIFO_REG register via the APB interface. The corresponding FIFO width is 32 bits and the depth is 512.

For DMA write operations to TX RAM, set up DMA linked list descriptors as described in Section 54.8.

### 54.6.2 RX RAM Module

There are two ways to enable a read operation: CPU and DMA read.

For CPU read operations from RX RAM, read the data directly from the SDHOST_BUFFIFO_REG register via the APB interface. The corresponding FIFO width is 32 bits and the depth is 512.

For DMA read operations from RX RAM, set up DMA linked list descriptors as described in Section 54.8.

## 54.7 DMA Linked List

Each unit in the linked list structure consists of two parts: a descriptor and a data buffer. In other words, each descriptor points to a unique data buffer and to the next descriptor in the linked list. Figure 54.7-1 shows the linked list.
```