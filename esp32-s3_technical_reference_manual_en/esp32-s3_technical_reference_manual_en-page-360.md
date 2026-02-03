**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Section Heading:**
3.4 Functional Description

**Subsection Heading and Content:**
3.4.1 Linked List

**Figure Caption with Diagrams:**
- Figure 3.4-1 shows the structure of a linked list.
- The diagram is labeled "Linked List" showing various data words (DW0, DW1, etc.) connected in sequence.

**Table Description and Content within Figure:**
- Table headers are as follows:
  - Owner
  - suc_eof
  - Reserved
  - err_eof
  - Reserved
  - length
  - size

- The table rows show the structure of a linked list descriptor, with fields like buffer address pointer.

**Figure Caption and Description for Figure:**
- "Figure 3.4-1 Structure of a Linked List"

**Body Text Explanation (with bullet points):**

- **Owner (DWO) [31]:** Specifies who is allowed to access the buffer that this descriptor points to.
  - Owner bits:
    - b0: CPU can access the buffer
    - b1: The GDMA controller can access the buffer

- When the GDMA controller stops using a buffer, it will be automatically cleared by hardware. This bit in transmit descriptors is set if the buffer has been received or transmitted.

- **GDMA_OUT_AUTO_WRBAC_KChn**:
  - Set to `1` when software loads a linked list.
  - Should also be set for receive channel registers (GDMA_IN).

- Note: GDMA_OUT prefix of transmit register channels, and GDMA_IN is the prefix of receive.

- **suc_eof (DWO) [30]:** Specifies whether the GDMA_IN_EOF_CHn_INT or GDMA_OUT_EOF_CHn_INT interrupt will be triggered when data corresponding to this descriptor has been received.
  - No interrupt after successful transfer; b1: An interrupt is set if a descriptor's success.

- **Reserved (DWO) [29]:** Reserved. Value of the bit does not matter in context provided here, but typically used for alignment or padding purposes within memory structures to ensure proper data handling and access by hardware components like GDMA.

- **err_eof (DWO) [28]:**
  - Specifies whether received data have errors.
  - Used only when UHCIO uses GDMA. When an error is detected, this bit indicates the end of one transfer phase in receive descriptors; set to `1` by hardware upon detection and clearing.

- **Reserved (DWO) [27:24]:** Reserved for future use or specific implementation details not detailed here but typically used as alignment bits within memory structures. 

**Footer Information:** 
Espressif Systems
360 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback