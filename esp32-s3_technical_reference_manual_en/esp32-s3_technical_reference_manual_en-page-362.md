**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Body Text with Subsections and Figures**

1. **Data Transfer Modes Description:**  
   As every transmit and receive channel can be used to access internal and external RAM, there are four data transfer modes:
   - from internal RAM to internal RAM
   - from internal RAM to external RAM
   - from external RAM to internal RAM
   - from external RAM to external RAM

2. **Section 3.4.4: Channel Buffer**  
   Every transmit and receive channel contains FIFOs at three levels, i.e., L1FIFO, L2FIFO, and L3FIFO. As Figure 3.4-2 shows, L1FIFO is close to the memory; L3FIFO is close to peripherals; and L2FIFO falls in between L1FIFO and L3FIFO.

   - **Figure Description:**
     - The figure illustrates a Channel Buffer with three levels labeled as Rx Channel Buffer (L1FIFO, L2FIFO), Tx Channel Buffer (L1FIFO, L2FIFO).
   
   Fixed depths for the FIFOs are:
   - L1FIFO and L3FIFO have fixed depth: 24
   - L2FIFO has a fixed depth of either 128 or 16 bytes.

3. **Section 3.4.5: Enabling GDMA**  
   Software uses the GDMA controller through linked lists.
   
   When the GDMA controller receives data, software loads an inlink, configures GDMA_INLINK_ADDR_CHn field with address of the first receive descriptor; and sets GDMA_INLINK_START_CHn bit to enable GDMA. 
   
   - **Figure Description:**
     - The figure illustrates a Channel Buffer (L1FIFO, L2FIFO) for transmitting data.
   
   When software loads an outlink:
   - prepares data
   - configures GDMA_OUTLINK_ADDR_CHn field with address of the first transmit descriptor; and sets GDMA_OUTLINK_START_CHn bit to enable GDMA. 
   - GDMA_INLINK_START_CHn, GDMA_OUTLINK_START_CHn bits are cleared automatically by hardware.
   
   In some cases:
   - To append more descriptors: clear the EOF bit in the final descriptor of an existing list and set its next descriptor address pointer (DW2) to the first descriptor for a new transfer. 
   - GDMA engine has specialized logic; if it is still ongoing, make sure to take appended descriptors into account.
   
   When using the Restart function:
   - software needs to rewrite addresses in the last descriptor of loaded list and set GDMA_INLINK_RESTART_CHn bit or GDMA_OUTLINK_RESTART_CHn (these two bits are cleared automatically by hardware).

**Footer:**
Espressif Systems  
362  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)