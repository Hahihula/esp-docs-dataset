**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Figure Caption and Diagram Description:**
- **Figure 20.5-2:** Communication Format of Parallel QSPI

**Body Text with Notes:**
ESP32 QSPI supports flash-read operation in one-line, two-line, and four-line modes. When working as a QSPI master, the command phase, address phase, dummy phase and data phase can be configured as needed, as flexible as in GP-SPI mode.

Note that GPI-SPI full-duplex mode does not support dummy phase.

**Subsection Title:**
20.6 GP-SPI Interrupt Hardware

**Body Text for Subsection 20.6:**
ESP32 SPI generates two types of interrupts. One is the SPI interrupt and the other is the SPI DMA interrupt.
ESP32 SPI reckons the completion of send- and/or receive-operations as the completion of one operation from the controller and generate one interrupt. When ESP32 SPI is configured to slave mode, the slave will generate read/write status registers and read/write buffer data interrupts according to different operations.

**Subsection Title:**
20.6.1 SPI Interrupts

**Body Text for Subsection 20.6.1:**
The SPI_*_INTEN bits in the SPI_SLAVE_REG register can be set to enable SPI interrupts. When an SPI interrupt happens, the interrupt flag in the corresponding SPI_*_DONE register will get set. This flag is writable, and an interrupt can be cleared by setting the bit to zero.
- **List of Interrupts:**
  - SPI_TRANS_DONE_INT: Triggered when an SPI operation is done.
  - SPI_SLV_WR_STA_INT: Triggered when an SPI slave status write is done.
  - SPI_SLV_RD_STA_INT: Triggered when an SPI slave status read is done.
  - SPI_SLV_WR_BUF_INT: Triggered when an SPI slave buffer write is done.
  - SPI_SLV_RD_BUD_INT: Triggered when an SPI slave buffer read is done.

**Subsection Title:**
20.6.2 DMA Interrupts

**Body Text for Subsection 20.6.2:**
SPI_OUT_TOTAL_EOF_INT: Triggered when all linked lists are sent.
- **List of Interrupts:**
  - SPI_OUT_EOF_INT: Triggered when one linked list is sent.
  - SPI_OUT_DONE_INT: Triggered when the last linked list item has zero length.
  - SPI_IN_SUC_EOF_INT: Triggered when all linked lists are received.

**Footer Information:**
Espressif Systems
362 ESP32 TRM (Version 5.6)
Submit Documentation Feedback