**Chapter Title:**
Chapter 19 UART Controller (UART)

**Section Titles and Descriptions with Registers Information**

- **Register Name:** UHCI_DMA_OUT_STATUS_REG (0x14)
  - **Description:** 
    - `UHCI_OUT_EMPTY`: DMA inlink descriptor's FIFO is empty. (RO)
    - `UHCI_OUT_FULL`: DMA outlink descriptor's FIFO is full. (RO)

- **Register Name:** UHCI_DMA_OUT_PUSH_REG (0x18)
  - **Description:**
    - `UHCI_OUTFIFO_PUSH`: Set this bit to push data into DMA FIFO. (R/W)
    - `UHCI_OUTFIFO_WDATA`: This is the data that need to be pushed into DMA FIFO. (R/W)

- **Register Name:** UHCI_DMA_IN_POP_REG (0x20)
  - **Description:**
    - `UHCI_INFO_POP`: Set this bit to pop data from DMA FIFO. (R/W)
    - `UHCI_INFO_RDATA`: This register stores the data popping from DMA FIFO. (RO)

**Footer Information:** 
- Page Number: 348
- Company Name: Espressif Systems
- Document Version and Type: ESP32 TRM (Version 5.6)