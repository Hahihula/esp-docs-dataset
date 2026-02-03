**Title: Chapter 32 USB On-The-Go (USB)**

---

### Figure Caption:
Figure 32.3-5. OTG_FS Interrupt Hierarchy

---

#### Text Content:

1. **Interrupt Sources**
   - When transmitting a packet using IN endpoints or OUT channels, the data payload’s address in memory should be written to the USB_HCDMA_n_REG (in Host mode) or USB_DPEDMA_n_REG (in Device mode) registers. When the endpoint or channel is enabled, the internal DMA will push the data payload from memory into the TX FIFO of the channel or endpoint.

2. **Interrupt Sources**
   - When receiving a packet using OUT endpoints or IN channels, the address of an empty buffer in memory should be written to the USB_HCDMA_n_REG (in Host mode) or USB_DPEDMA_n_REG (in Device mode) registers. When the endpoint or channel is enabled, the internal DMA will pop the data payload from RX FIFO into the buffer.

---

#### Subtitle:
32.3.5.3 Scatter/Gather DMA Mode

---

#### Text Content:

When operating in Scatter/Gather DMA mode, buffers containing data payloads can be scattered throughout memory. Each endpoint or channel will have a contiguous DMA descriptor list, where each descriptor contains a 32-bit pointer to the data payload buffer and a 32-bit buffer descriptor (BufferStatus Quadlet). The data payloads and buffers can correspond to a single transaction (<1 MPS bytes) or an entire transfer (>1 MPS bytes). (MPS: maximum packet size) The list is implemented as a ring buffer meaning that the DMA will return to the first entry when it encounters the last entry on the list.

- When transmitting a transfer/transaction using IN endpoints or OUT channels, the DMA will gather the data payloads from the multiple buffers and push them into a TX FIFO. 

---

**Footer:**
Espressif Systems  
1234  
ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback