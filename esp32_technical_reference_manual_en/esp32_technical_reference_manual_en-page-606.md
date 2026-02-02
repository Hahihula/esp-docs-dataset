**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Titles and Content:**

#### **27.9.1 DMAC Initialization**
The DMAC initialization should proceed as follows:
- Write to the DMAC Bus Mode Register (BMOD_REG) will set the Host bus's access parameters.
- Write to the DMAC Interrupt Enable Register (IDINTEN) will mask any unnecessary interrupt causes.

The software driver creates either the transmit or receive descriptor list. Then, it writes to the DMAC Descriptor List Base Address Register (DBADDR), providing the DMAC with the starting address of the list.

The DMAC engine attempts to acquire descriptors from descriptor lists.

#### **27.9.2 DMAC Transmission Initialization**
The DMAC transmission occurs as follows:
1. The Host sets up the elements (DESO-DES3) for transmission, and sets the OWN bit (DESO[31]). The Host also prepares the data buffer.
2. The Host programs the write-data command in the CMD register in BIU.
3. The Host also programs the required transmit threshold (TX_WMARK field in FIFO register).
4. The DMAC engine fetches the descriptor and checks the OWN bit. If the OWN bit is not set, it means that the host owns the descriptor. In this case, the DMAC enters a suspend-state and asserts the Descriptor Unable interrupt in the IDSTS register. In such a case, the host needs to release the DMAC by writing any value to PLDMND_REG.
5. It then waits for the Command Done (CD) bit and no errors from BIU, which indicates that a transfer can be done.

Subsequently, the DMAC engine waits for a DMA interface request (dw_dmac_req) from BIU. This request will be generated, based on the programmed transmit-threshold value. For the last bytes of data which cannot be accessed using a burst, single transfers are performed on the AHB Master Interface.
7. The DMAC fetches the transmit data from the data buffer in the Host memory and transfers them to FIFO for transmission to card.

When data span across multiple descriptors, the DMAC fetches the next descriptor and extends its operation using the following descriptor. The last descriptor bit indicates whether the data span multiple descriptors or not.
9. When data transmission is complete, the status information is updated in the IDSTS register by setting the Transmit Interrupt, if it has already been enabled. Also, the OWN bit is cleared by the DMAC by performing a write transaction to DESO.

#### **27.9.3 DMAC Reception Initialization**
The DMAC reception occurs as follows:
1. The Host sets up the element (DESO-DES3) for reception, and sets the OWN bit (DESO[31]).
2. The Host programs the read-data command in the CMD register in BIU.
3. Then, the Host programs the required level of the receive-threshold (RX_WMARK field in FIFO register).

**Footer:**
Espressif Systems  
606  
Submit Documentation Feedback

ESP32 TRM (Version 5.6)