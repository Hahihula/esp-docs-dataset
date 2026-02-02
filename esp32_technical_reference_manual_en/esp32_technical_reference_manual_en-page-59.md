**Chapter Title: Chapter 2 DMA Controller (DMA)**

---

**Body Text:**

Before DMA transmits data, software must initialize the transmit-linked-list and the data to be transferred. UHCI_ OUTLINK_ADDR is used to point to the first out_link descriptor. The register must be programmed with the lower 20 bits of the address of the initial transmit-linked-list item. After UHCI_COUTLINK_START is set, the DMA Engine will read data from the RAM location specified by the linked-list descriptor and then transfer the data through the Encoder. The DMA Engine will then shift the data out serially through the UART transmitter.

The UART DMA follows a format of (separator + data + separator). The Encoder is used for adding separators before and after data, as well as using special-character sequences to replace data that are the same as separators. The Decoder is used for removing separators before and after data, as well as replacing the special-character sequences with separators. There can be multiple consecutive separators marking the beginning or end of data. These separators can be configured through UHCI_SEPER_CH, with the default values being 0xC0. Data that are the same as separators can be replaced with UHCI_ESCSEQUO_CHARO (0xDB by default) and UHCI_ESCSEQUO_CHAR1 (0xdd by default). After the transmission process is complete, a UHCI_OUT_TOTAL_EOF_INT interrupt will be generated. After the reception procedure is complete, a UHCI_IN_ SUC_EOF_INT interrupt will be generated.

**Note:**
Please note that the buffer address pointer field in in_link descriptors should be word-aligned, and the size field in the last_in_link descriptor should be at least 4 bytes larger than the length of received data.

---

**Section Title: 2.5 SPI DMA Interface**

---

**Diagram Description (Figure Caption): Figure 2.5-1. SPI DMA**

**Diagram Content Summary:** The diagram shows a block diagram for SPI DMA interface with connections between different components such as DMA, SPI0_CHAN_SEL, SPI1_CHAN_SEL, SPI2_CHAN_SEL, and SPI3_CHAN_SEL.

**Body Text:**
ESP32 SPI modules can use DMA as well as the CPU for data exchange with peripherals. As can be seen from Figure 2.5-1, two DMA channels are shared by SPI1, SPI2 and SPI3 controllers. Each DMA channel can be used by any one SPI controller at any given time.

The ESP32 SPI DMA Engine also uses a linked list to receive/transmit data. Burst transmission is supported. The data size for a single transfer must be four bytes aligned. Consecutive data transfer is also

---

**Footer:**
Espressif Systems
59
Submit Documentation Feedback
ESP32 TRM (Version 5.6)