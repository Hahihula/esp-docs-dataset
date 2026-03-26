

```markdown
## 50.4.5 Slave Mode and DMA Modes

OTG_FS supports three ways to access memory: Slave mode, Buffer DMA mode, and Scatter/Gather DMA mode.

### 50.4.5.1 Slave Mode

In Slave mode, all data payloads must be pushed/popped to and from the FIFOs by the CPU.

- When transmitting a packet using IN endpoints or OUT channels, the data payload must be pushed into the corresponding endpoint or channel's TX FIFO.
- When receiving a packet, the packet's status entry must first be popped off the RX FIFO by reading USB_GRXSTSP_REG. The status entry should be used to determine the length of the packet's payload (in bytes). The corresponding number of bytes must then be manually popped off the RX FIFO by CPU reading from the RX FIFO's memory region.

### 50.4.5.2 Buffer DMA Mode

Buffer DMA mode is similar to Slave mode but utilizes the internal DMA to push and pop data payloads to the FIFOs.

- When transmitting a packet using IN endpoints or OUT channels, the data payload's address in memory should be written to USB_HCDMANn_REG in Host mode or USB_DIEPDMan_REG in Device mode. When the endpoint or channel is enabled, the internal DMA will push the data payload from memory into the TX FIFO of the channel or endpoint.
- When receiving a packet using OUT endpoints or IN channels, the address of an empty buffer in memory should be written to USB_HCDMANn_REG in Host mode or USB_DOEPDMAn_REG in Device mode. When the endpoint or channel is enabled, the internal DMA will pop the data payload from RX FIFO into the buffer.

### 50.4.5.3 Scatter/Gather DMA Mode

Figure 50.4-6. Scatter/Gather DMA Descriptor List
```