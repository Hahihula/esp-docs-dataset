**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Section Title:**
34.8 The Structure of DMA Descriptor Chain

**Body Text:**
Each linked list consists of four words. As is shown below, Figure 34.8-1 demonstrates the linked list’s structure, and Table 34.8-1, Table 34.8-2, Table 34.8-3, Table 34.8-4 provide the descriptions of linked lists.

**Figure Caption:**
Figure 34.8-1 The Structure of a Linked List

**Table Title and Description:**
The DESO element contains control and status information.
Table 34.8-1 Word DESO of SD/MMC DMA Linked List
- **Bits**: 
  - Name:
    - 31: OWNER (When set, this bit indicates that the descriptor is owned by the DMA Controller. When reset, it indicates that the descriptor is owned by the Host. The DMA clears this bit when it completes the data transfer.)
    - 30: CES (Card Error Summary)
      - EBE: End Bit Error
      - RTO: Response Time out
      - RCRC: Response CRC
      - SBE: Start Bit Error
      - DRTO: Data Read Timeout
      - DCRC: Data CRC for Receive
      - RE: Response Error
    - 29-6: Reserved (When set, this bit indicates that the descriptor list has reached its final descriptor. The DMA Controller then returns to the base address of the list, creating a Descriptor Chain.)
    - 5: ER (End of Ring) (These error bits indicate the status of the transition to or from the card.)

**Footer Information:**
Espressif Systems
1276 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback