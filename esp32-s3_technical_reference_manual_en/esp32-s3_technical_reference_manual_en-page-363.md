**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Figure Caption and Diagram Description:**
- Figure caption: "Relationship among Linked Lists"
- The diagram shows a linked list structure with elements labeled as "Next descriptor address" connected to each other.

**Section Heading:**
3.4.6 Linked List Reading Process

**Body Text:**
Once configured and enabled by software, the GDMA controller starts to read the linked list from internal RAM.
The GDMA performs checks on descriptors in the linked list. Only if the descriptors pass these checks will it transfer data corresponding to the GDMA channel.

If any of the descriptors fail their respective hardware trigger descriptor error interrupts (either GDMA_IN_DSCR_ERR_CHn_INT or GDMA_OUT_DSCR_ERR_CHn_INT), and then halt further operations on that particular channel.
The checks performed are:
- **Owner bit check**: When GDMA_IN_CHECK_OWNER_CHn or GDMA_OUT_CHECK_OWNER_CHn is set to 1. If the owner bit equals zero, it indicates access by CPU; otherwise fails this step of validation.

**Subsection Heading:**
3.4.7 EOF

**Body Text:**
The GDMA controller uses EOF (end-of-frame) flags for indicating end-of-segment transfers corresponding specific descriptors.
- Before transmitting data via GDMA_OUT_TOTAL_EOF_CHn_INT, the bit should be set to enable GDMA_OUT_TOTAL_EOF_CHn_INT interrupt if data in buffer has been transmitted; otherwise, a GDMA_OUT_TOTAL_EOF_CHn_INT interrupt is generated.

**Additional Information:**
Before receiving new data from channel connected UHCI0, GDMA_IN_ERR_CHn_EOF_INT supports interrupts for error handling. This feature ensures proper functioning and recovery upon detecting errors during transmission or reception processes.
  
**Footer Text:** 
Espressif Systems
363 ESP32-S3 TRM (Version 1.7)