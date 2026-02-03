**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Table Header:**
- Bits | Name | Description

**Table Content:**
- **Bits:** 31:0  
- **Name:** Next Descriptor Address  
- **Description:** If CH (DESO[4]) is set, this bit contains the address pointer to the next descriptor. If this is not the last descriptor in a chained descriptor structure, the address pointer to the next descriptor should be: DES3[1:0] = 0.

**Section Title and Subsection Titles with Content:**

**34.9 Initialization**
- **Subsection:** 34.9.1 DMA Initialization
  - The DMA Controller initialization should proceed as follows:
    1. Write to the DMA Bus Mode Register (SDHOST_BMOD_REG) will set the Host bus's access parameters.
    2. Write to the DMA Interrupt Enable Register (SDHOST_IDINTEN_REG) will mask any unnecessary interrupt causes.
    3. The software driver creates either the inlink or the outlink descriptors. Then, it writes to the DMA Descriptor List Base Address Register (SDHOST_DBADDR_REG), providing the DMA Controller with the starting address of the list.
    4. The DMA Controller engine attempts to acquire descriptors from descriptor lists.

**Subsection:** 34.9.2 DMA Transmission Initialization
- The DMA transmission occurs as follows:
  - **Step 1:** The Host sets up the elements (DESO-DES3) for transmission, and sets the OWNER bit (DESO[31]). The Host also prepares the data buffer.
  - **Step 2:** The Host programs the write-data command in the CMD register in BIU.
  - **Step 3:** The Host also programs the required transmit threshold (SDHOST_TX_WMARK field in SDHOST_FIFO_TH register).
  - **Step 4:** The DMA Controller engine fetches the descriptor and checks the OWNER bit. If the OWNER bit is not set, it means that the host owns the descriptor. In this case, the DMA Controller enters a suspend-state and asserts the Descriptor Unable interrupt in the SDHOST_IDSTS_REG register. In such a case, the host needs to release the DMA Controller by writing any value to SDHOST_PLDMND_REG.
  - **Step 5:** It then waits for the Command Done (CD) bit in DHOST_RINTSTS_REG register and no errors from BIU, which indicates that a transfer has completed.
  - **Step 6:** Subsequently, the DMA Controller engine waits for a DMA interface request from BIU. This request will be generated, based on the programmed transmit-threshold value. For the last bytes of data which cannot be accessed using a burst, single transfers are performed on the AHB Master Interface.
  - **Step 7:** The DMA Controller fetches the transmit data from the data buffer in the Host memory and transfers them to RAM for transmission to card.

**Footer:**
Espressif Systems  
1278  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)