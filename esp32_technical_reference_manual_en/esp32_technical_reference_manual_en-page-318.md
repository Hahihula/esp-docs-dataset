**Chapter Title:**
Chapter 19 UART Controller (UART)

**Subheading and List of Interrupts with Descriptions for UHCI:**

- **19.3.10 UHCI Interrupts**
  - **UHCI_SEND_A_REG_Q_INT:** Triggered when using the always_send registers to send a series of short packets, this is triggered when DMA has sent a short packet.
  - **UHCI_SEND_S_REG_Q_INT:** Triggered when using the single_send registers to send a series of short packets; this is triggered when DMA has sent a short packet.
  - **UHCI_OUT_TOTAL_EOF_INT:** Triggered when all data have been sent.
  - **UHCI_OUTLINK_EOF_ERR_INT:** Triggered when there are some errors in EOF in the outlink descriptor.
  - **UHCI_IN_DSCR_EMPTY_INT:** Triggered when there are not enough inlinks for DMA.
  - **UHCI_OUT_DSCR_ERR_INT:** Triggered when there are some errors in the inlink descriptor.
  - **UHCI_IN_DSCR_ERR_INT:** Triggered when there are some errors in the outlink descriptor.
  - **UHCI_OUT_EOF_INT:** Triggered when the current descriptor’s EOF bit is set to 1.
  - **UHCI_OUT_DONE_INT:** Triggered when an outlink descriptor is completed.
  - **UHCI_IN_ERR_EOF_INT:** Triggered when there are some errors in EOF in the inlink descriptor.
  - **UHCI_IN_SUC_EOF_INT:** Triggered when a data packet has been received.
  - **UHCI_IN_DONE_INT:** Triggered when an inlink descriptor has been completed.
  - **UHCI_TX_HUNG_INT:** Triggered when DMA takes much time to read data from RAM.
  - **UHCI_RX_HUNG_INT:** Triggered when DMA takes too long a time to receive data .
  - **UHCI_TX_START_INT:** Triggered when DMA detects a separator char.
  - **UHCI_RX_START_INT:** Triggered when a separator char has been sent.

**Section Title:**
19.4 Register Summary

**Subsection and Table for UART Register Summary**

- **19.4.1 UART Register Summary**
  The addresses in this section are relative to the UART base address provided in Table 3.3-6 in Chapter 3 System and Memory.
  
  - *The abbreviations given in Column Access* are explained in Section [Access Types for Registers](#).

**Table:**

| Name | Description | UART0 | UART1 | UART2 | Acc |
|------|-------------|-------|-------|-------|-----|
| Configuration registers | | | | | |
  - **UART_CONF0_REG:** Configuration register, address range is `0x3FF40020` to `0x3FF50020`, access type: R/W

**Footer Information:**
Espressif Systems  
Page number and document version information at the bottom.