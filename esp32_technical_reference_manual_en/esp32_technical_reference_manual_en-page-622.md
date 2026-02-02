**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

**Register Information:**
- **Register Name:** FIFOth_Reg (0x004c)
- **Field Description:**
  - **DMA_Multiple_Transaction_Size**: Burst size of multiple transaction, should be programmed same as DMA controller multiple-transaction-size SRC/DEST_MSIZE. 
    - 000: 1-byte transfer
    - 001: 4-byte transfer
    - 010: 8-byte transfer
    - 011: 16-byte transfer
    - 100: 32-byte transfer
    - 101: 64-byte transfer
    - 110: 128-byte transfer
    - 111: 256-byte transfer (R/W)

**Field Values and Reset Value:**
- **Values:** 31, 30, ..., 0x0000
- **Reset Value:** 0

**Field Name with Reserved Indication:**
- RX_WMARK (reserved)
- TX_WMARK (reserved)

**Field Description for DMA_Multiple_Transaction_Size:**
- FIFO threshold watermark level when receiving data to card. When FIFO data count reaches greater than this number, DMA/FIFO request is raised.
  - During end of packet, request is generated regardless of threshold programming in order to complete any remaining data.

**Field Description for RX_WMARK (Non-DMA mode):**
- When FIFO threshold (RXDR) interrupt is enabled and RX_WMARK is reached or exceeded during a packet transfer. Interrupt not generated if the host reads more than one byte from the card.
  - During end of packet, request to DMA controller.

**Field Description for TX_WMARK:**
- FIFO threshold watermark level when transmitting data to card:
  - When FIFO data count reaches RX_TX_WMARK and DMA/FIFO request is raised. If interrupt enabled during transmission or at the beginning of a new packet.
    - During end of packet, request generated regardless if threshold programming.

**Field Description for TX_WMARK (Non-DMA mode):**
- When transmit FIFO threshold (TXDR) interrupt not disabled:
  - During last interrupt generation DMA controller is responsible to fill FIFO with remaining bytes before FIFO becomes full or CIU completes data transfers.
    - In DMA mode, at the end of packet transfer if less than burst size.

**Footer Information:**
- **Company:** Espressif Systems
- **Page Number:** 622
- **Document Version:** ESP32 TRM (Version 5.6)
- **Links:** Submit Documentation Feedback