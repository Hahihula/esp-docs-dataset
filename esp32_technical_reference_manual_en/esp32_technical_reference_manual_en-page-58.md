**Chapter 2: DMA Controller (DMA)**

- **owner (DWO) [31]:** The allowed operator of the buffer corresponding to the current linked list.
  - `1'b0`: the allowed operator is the CPU;
  - `1'b1`: the allowed operator is the DMA controller.

- **eof (DWO) [30]:** End-Of-File character.
  - `1'b0`: the linked-list item does not mark the end of the linked list;
  - `1'b1`: the linked-list item is at the end of the linked list.

- **reserved (DWO) [29:24]:** Reserved bits. Software should not write to this space.
  
- **length (DWO) [23:12]:** The number of valid bytes in the buffer corresponding to the current linked list.
  - *NOTE:* This is a word-aligned field.

- **size (DWO) [11:0]:** The size of the buffer corresponding to the current linked list. 
  - *NOTE:* The size must be word-aligned and this address points directly into the data buffer, not an offset from it.
  
- **buffer address pointer (DW1):** Buffer address pointer.

When receiving data:
- If the data transfer length is smaller than specified by the buffer size, DMA will use remaining space. This enables the DMA engine to be used for transferring arbitrary number of bytes.


**2.4 UART DMA (UDMA)**

The ESP32 has three UART interfaces that share two UDMA (UART DMA) controllers.
- The `UHCI_UARTx_CE` is 0, 1, or 2 and it's selected by the UART controller to use.

![Figure 2.4-1: Data Transfer in UDMA Mode](image)

**Figure Description:** 
- **Figure 2.4-1 shows the data transfer in UDMA mode.**
- Before the DMA Engine receives data:
  - Software must initialize the receive-linked-list.
  - `UHCI_INLINK_ADDR` is used to point to the first in_link descriptor.

The register must be programmed with lower 20 bits of address for initial linked-list item:

- After setting `UHCI_INLINK_START`, UHC will transmit data received by UART to the Decoder. 
- Data parsed after being stored into RAM as specified receive-linked-list descriptor.


**Footer:**
- Espressif Systems
- ESP32 TRM (Version 5.6)
- Submit Documentation Feedback