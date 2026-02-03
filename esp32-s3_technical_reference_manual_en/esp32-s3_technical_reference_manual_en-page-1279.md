**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Section Heading and Subsection with Content:**

**34.9.3 DMA Reception Initialization**

The DMA reception occurs as follows:

1. The Host sets up the element (DESO-DES3) for reception, and sets the OWNER bit (DESO[31]).

2. The Host programs the read-data command in the CMD register in BIU.

3. Then, the Host programs the required level of the receive-threshold (SDHOST_RX_WMARK field in SDHOST_FIFOth_REG register).

4. The DMA Controller engine fetches the descriptor and checks the OWNER bit. If the OWNER bit is not set, it means that the host owns the descriptor. In this case, the DMA enters a suspend-state and asserts the Descriptor Uninterruptible in the SDHOST_IDSTS_REG register. In such a case, the host needs to release the DMA Controller by writing any value to SDHOST_PLDMND_REG.

5. It then waits for the Command Done (CD) bit no errors from BIU, which indicates that a reception can be done.

6. The DMA Controller engine then waits for a DMA interface request from BIU. This request will be generated, based on the programmed receive-threshold value. For the last bytes of the data which cannot be accessed using a burst, single transfers are performed on the AHB.

7. The DMA Controller fetches the data from RAM and transfers them to the Host memory.

8. When data span across multiple descriptors, the DMA Controller will fetch the next descriptor and extend its operation using the following descriptor. The last descriptor bit indicates whether the data span multiple descriptors or not.
   - Note: This point is repeated in a different context later on with additional details about setting SDHOST_IDSTS_RI.

9. When data reception is complete, the status information is updated in the SDHOST_IDSTS_REG register by setting SDHOST_IDSTS_RI, if it has already been enabled. Also, the OWNER bit is cleared by the DMA Controller by performing a write-transaction to DESO.

**34.10 Clock Phase Selection**

If the setup time requirements for the input or output data signal are not met, users can specify the clock phase, as shown in the figure 34.10-1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)