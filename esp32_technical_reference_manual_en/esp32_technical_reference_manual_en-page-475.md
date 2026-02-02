**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Titles and Subtitles:**
- **24.8 Linked List Descriptors**

This section shows the structure of the linked lists and the descriptors. Every linked list consists of eight words.

- **24.8.1 Transmit Descriptors**

The structure of the transmitter linked lists is shown in Figure 24.8-1. Table 24.8-1 to Table 24.8-4 show the description of the linked lists.

**Figure Title:**
Figure 24.8-1. Transmit Descriptor

**Table Titles and Content:**

- **Table 24.8-1. Transmit Descriptor O (TDESO)**
  - Bits | Name | Description
  - [31] | OWN: Own Bit | When set, this bit indicates that the descriptor is owned by the DMA. When this bit is reset, it indicates that the descriptor is owned by the Host. The DMA clears this bit, either when it completes the frame transmission or when the buffers allocated to the descriptor are empty. The ownership bit of the First Descriptor of the frame should be set after all subsequent descriptors belonging to the same frame have been set. This avoids a possible race condition between fetching a descriptor and the driver setting an ownership bit.
  - [30] | IC: Interrupt on Completion | When set, this bit sets the Transmit Interrupt (Register 5[0]) after the present frame has been transmitted. This bit is valid only when the last segment bit (TDESO[29]) is set.
  - [29] | LS: Last Segment | When set, this bit indicates that the buffer contains the last segment of the frame. When this bit is set, the TBS1 or TBS2 field in TDES1 should have a non-zero value.
  - [28] | FS: First Segment | When set, this bit indicates that the buffer contains the first segment of a frame.

**Footer Information:**
Espressif Systems
475 ESP32 TRM (Version 5.6)