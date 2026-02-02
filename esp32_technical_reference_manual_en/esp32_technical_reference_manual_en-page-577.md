**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Menu/Navigation Link:**
GoBack

**Table Title and Description:**
Register 26.5, SLCINT_CLR_REG (0x10)
- The table lists various interrupt clear bits for different operations related to the slave controller.

**Table Content Summary:**

| Bit Number | Name                          |
|------------|-------------------------------|
| 31         | SLCOINT_SLCO_RX_DSCR_ERR_INT_CLR |
|           | Interrupt clear bit for Slave sending linked list descriptor error. (WO) |
| 27-0       | Reserved                      |

**Interrupt Clear Bits Description:**

- **SLCOINT_SLCO_RX_DSCR_ERR_INT_CLR:** Interrupt clear bit for Slave sending linked list descriptor error.
- **SLCOINT_SLCO_TX_DSCR_ERR_INT_CLR:** Interrupt clear bit for Slave receiving linked list descriptor error. (WO)
- **SLCOINT_SLCO_RX_EOF_INT_CLR:** Interrupt clear bit for Slave sending operation completion. (WO)
- **SLCOINT_SLCO_RX_DONE_INT_CLR:** Interrupt clear bit for single buffer's sent interrupt, in Slave sending mode.
- **SLCOINT_SLCO_TX_SUC_EOF_INT_CLR:** Interrupt clear bit for Slave receiving operation completion.

**Additional Interrupt Clear Bits:**

- SLCOINT_SLCO_TXDone_INT_CLR
- SLCOINT_SLCO_RX_OVF_INT_CLR (Set this bit to clear the Slave receiving overflow interrupt. (WO))
- SLCOINT_SLCO_RX_UDF_INT_CLR (Set this bit to clear the Slave sending underflow interrupt.)
- SLCOINT_SLCO_TX_START_INT_CLR (Set this bit to clear the interrupt for Slave receiving operation initialization.)

**Interrupt Clear Bits Continued:**

- **SLCOINT_SLC_FROSHOST_BIT7_INT_CLR:** Set this bit to clear the SLCINT_SLC_FRHOST_BIT7_INTERRUPT.
- **SLCOINT_SLC_FROSHOST_BIT6_INT_CLR:** Set this bit to clear the SLCOINT_SLC_FRHOST_BIT6_INTERRUPT.
- **SLCOINT_SLC_FROSHOST_BIT5_INT_CLR:** Set this bit to clear the SLCINT_SLC_FRHOST_BIT5_INTERRUPT.
- **SLCOINT_SLC_FROSHOST_BIT4_INT_CLR:** Set this bit to clear the SLCOINT_SLC_FRHOST_BIT4_INTERRUPT.

**Footer:**
Continued on the next page...

**Document Information:**
Espressif Systems
Page 577, ESP32 TRM (Version 5.6)
Submit Documentation Feedback