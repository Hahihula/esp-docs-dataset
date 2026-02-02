**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Section Titles and Descriptions with Registers Information:**

1. **Register Description:** 
   - Register Name: `I2S_OUT_EOF_DESC_ADDR_REG`
   - Offset Address: `(0x038)`
   - Description: "The address of outlink descriptor that produces EOF."
   - Access Type: (RO)
   
2. **Register Description:**
   - Register Name: `I2S_IN_EOF_DESC_ADDR_REG`
   - Offset Address: `(0x03c)`
   - Description: "The address of inlink descriptor that produces EOF."
   - Access Type: (RO)

3. **Register Description:** 
   - Register Name: `I2S_OUT_EOF_BFR_DESC_ADDR_REG`
   - Offset Address: `(0x040)`
   - Description: "The address of the buffer corresponding to the outlink descriptor that produces EOF."
   - Access Type: (RO)

4. **Register Description:** 
   - Register Name: `I2S_INLINK_DSCR_REG`
   - Offset Address: `(0x048)`
   - Description: "The address of current inlink descriptor."
   - Access Type: (RO)

5. **Register Description:** 
   - Register Name: `I2S_INLINK_DSCR_BFO_REG`
   - Offset Address: `(0x04c)`
   - Description: "The address of next inlink descriptor."
   - Access Type: (RO)

6. **Register Description:** 
   - Register Name: `I2S_INLINK_DSCR_BF1_REG`
   - Offset Address: `(0x050)`
   - Description: "The address of next inlink data buffer."
   - Access Type: (RO)

**Footer Information:**
- Company: Espressif Systems
- Document Version and Title: ESP32 TRM (Version 5.6)
- Page Number: 441

**Navigation Link:** 
- GoBack