**Title: Chapter 26 SDIO Slave Controller (SDIO)**

**Subtitle: Register 26.4. SLCOINT_ENA_REG (0xC)**

**Table Description:**  
The table lists various interrupt enable bits for the slave controller, each associated with a specific function and register bit number.

- **Bit Number**: The column on the left shows the numerical position of each bit in the register.
- **Interrupt Name**: Each row contains an interrupt name followed by its description. Examples include:
  - `SLCOINT_SLCO_RX_DSCR_ERR_INT_ENA`: Interrupt enable for slave sending linked list descriptor error (R/W).
  - `SLCOINT_SLCO_TX_DSCR_ERR_INT_ENA`: Interrupt enable bit for slave receiving linked list descriptor error.
  - `SLCOINT_SLCO_RX_EOF_INT_ENA`: Interrupt enable bit for slave sending operation completion.

**Interrupt Enable Bits Description:**
- Each interrupt name is followed by a description of its function, such as:
  - Slave sending mode (R/W).
  - Slave receiving buffer overflow or underflow.
  - Host to interrupt slave communication events like start and error conditions. 

**Example Entries from the Table:**  
1. `SLCOINT_SLCO_RX_DSCR_ERR_INT_ENA`: The interrupt enable bit for Slave sending linked list descriptor error (R/W).
2. `SLCOINT_SLCO_TX_DSCR_ERR_INT_ENA`: The interrupt enable bit for Slave receiving linked list descriptor error.
3. `SLCOINT_SLCO_RX_EOF_INT_ENA`: The interrupt enable bit for Slave sending operation completion.

**Additional Information:**
- There is a note at the bottom indicating that this information pertains to "Espressif Systems ESP8266 TRM (Version 5.6)".
  
**Navigation Link:** 
- A link labeled "GoBack" in blue text on the top right corner of the page.

This structured description should help any pure text model understand and answer questions related to this image content accurately without needing visual inspection directly from an image source itself.