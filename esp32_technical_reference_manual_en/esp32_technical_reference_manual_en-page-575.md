**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Menu:**
GoBack

**Table Title:**
Register 26.3. SLCOINT_ST_REG (0x8)

**Table Description and Values:**
- The table lists various interrupt status bits for different operations related to the SDIO Slave Controller.
- Each row corresponds to a specific bit in the register, with descriptions of what each bit indicates.

**List Items Descriptions from Top to Bottom:**

1. **SLCOINT_SLC0_RX_ERR_INT_ST (RO)**
   - The interrupt status bit for Slave sending descriptor error.

2. **SLCOINT_SLC0_TX_DSCR_INT_ST (RO)**
   - The interrupt status bit for Slave receiving descriptor error.

3. **SLCOINT_SLC0_RX_EOF_INT_ST (RO)**
   - The interrupt status bit for finished Slave sending operation.

4. **SLCOINT_SLC0_RX_DONE_INT_ST (RO)**
   - The interrupt status bit for finished Slave sending operation as finished.

5. **SLCOINT_SLC0_TX_SUC_EOF_INT_ST (RO)**
   - The interrupt status bit for marking Slave receiving operation during the receiving operation, marked when a single buffer is done finishing its transfer to Host memory or when all buffers are transferred and the transfer completes with no errors.
   
6. **SLCOINT_SLC0_TX_DONE_INT_ST (RO)**
   - The interrupt status bit for marking a single buffer as finished.

7. **SLCOINT_SLC0_TX_OVF_INT_ST (RO)**
   - The interrupt status bit for Slave receiving overflow interrupt, indicating that the slave has received more data than it can handle and is overflowing its internal buffers.
   
8. **SLCOINT_SLC0_RX_UDF_INT_ST (RO)**
   - The interrupt status bit for Slave sending buffer underflow.

9. **SLCOINT_SLC0_TX_START_INT_ST (RO)**
   - The interrupt status bit for Slave receiving interrupt initialization, indicating that the slave has started to receive data from Host memory.
   
10. **SLCOINT_SLC_FROHOST_BIT7_INT_ST (RO)**
    - The interrupt status bit 7 for Host to interrupt Slave.

11. **SLCOINT_SLC_FROHOST_BIT6_INT_ST (RO)**
    - The interrupt status bit 6 for Host to interrupt Slave.
    
12. **SLCOINT_SLC_FROHOST_BIT5_INT_ST (RO)**
    - The interrupt status bit 5 for Host to interrupt Slave.

13. **SLCOINT_SLC_FROHOST_BIT4_INT_ST (RO)**
    - The interrupt status bit 4 for Host to interrupt Slave.
    
14. **SLCOINT_SLC_FROHOST_BIT3_INT_ST (RO)**
    - The interrupt status bit 3 for Host to interrupt Slave.

15. **SLCOINT_SLC_FROHOST_BIT2_INT_ST (RO)**
    - The interrupt status bit 2 for Host to interrupt Slave.
    
16. **SLCOINT_SLC_FROHOST_BIT1_INT_ST (RO)**
    - The interrupt status bit 1 for Host to interrupt Slave.

17. **SLCOINT_SLC_FROHOST_BIT0_INT_ST (RO)**
    - The interrupt status bit 0 for Host to interrupt Slave.
    
**Footer:**
Espressif Systems
575 ESP32 TRM (Version 5.6)
Submit Documentation Feedback