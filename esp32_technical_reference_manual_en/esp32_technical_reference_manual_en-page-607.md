**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Body Text with Numbered List:**

4. The DMAC engine fetches the descriptor and checks the OWN bit. If the OWN bit is not set, it means that the host owns the descriptor. In this case, the DMA enters a suspend-state and asserts the Descriptor Unable interrupt in IDSTS register. In such cases, if there needs to release the DMAC by writing any value to PLDMND_REG.

5. It then waits for the Command Done (CD) bit and no errors from BIU, which indicates that a transfer can be done.

6. The DMAC engine then waits for a DMA interface request (dw_dma_req) from BIU. This request will be generated based on the programmed receive-threshold value. For the last bytes of data cannot be accessed using burst transfers are performed on AHB.

7. The DMAC fetches the data from FIFO and transfers them to Host memory.

8. When data span across multiple descriptors, the DMAC will fetch the next descriptor and extend its operation using the following descriptor bit indicates whether the data span multiple descriptors or not.
   - Last descriptor bit

9. When data reception is complete, the status information updated in the IDSTS register by setting Receive-Interrupt if it has already been enabled Also, the OWN bit cleared by DMAC performing a write transaction to DESO.

**Subsection Title:**
2710 SD/MMC Timing

**Figure Description and Caption with Diagram (Figure 2710-1):**

Figure caption:
SD/MMC in high-speed mode. Table lists timing requirements for ensuring reliable communication.
Table description:

**Table Title:** 
Table 2710-1: SD/MMC Timing Requirements 

| Symbol | Parameter       | Conditions     | Min   | Typ    | Max   | Unit |
|--------|-----------------|----------------|-------|--------|-------|------|
| t<sub>W(CKL)</sub> | Clock Low Time  | f<sub>PP</sub> = 80 MHz | —    | 12.5 ns | —    | ns   |
| t<sub>W(CKH)</sub> | Clock High Time | f<sub>PP</sub> = 80 MHz | —    | 12.5 ns | —    | ns   |
| t<sub>ISU</sub>     | Input Setup Time in HS Mode | f<sub>PP</sub> = 80 MHz | 3.4 ns | —    | —    | ns   |
| t<sub>IH</sub>      | Input Hold Time in HS Mode | f<sub>PP</sub> = 80 MHz | 1.1 ns | —    | —    | ns   |
| t<sub>OV</sub>       | Output Valid Time in HS Mode | f<sub>PP</sub> = 80 MHz | —    | 5.9 ns | —    | ns   |

**Footer:**
Espressif Systems
607 ESP32 TRM (Version 5.6)
Submit Documentation Feedback