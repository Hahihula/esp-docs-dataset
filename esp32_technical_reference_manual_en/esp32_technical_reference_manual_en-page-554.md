**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** GoBack

**Section Header and Register Information:**
- **Register Description**: 
  - "Register 25.9. TWAI_DATA_4_REG (0x0050)"
  
**Field Descriptions with Binary Representation, Mask Values, and Reset Value in Red Text on the Right Side of Each Field:**

1. **TWAI_TX_BYTE_4**
   - Description: Stored the 4th byte information of the data to be transmitted under operating mode (WO)
   - Binary Representation: `0 0 0 0 0 0 0 0`
   - Mask Value in Red Text on Right Side: `[TWAI_ACCEPTANCE_MASK_0]`
   - Reset Value in Blue Text at Bottom Left of Field: `Reset`

2. **TWAI ACCEPTANCE MASK_0**
   - Description: Stored the Oth byte of the filter code under reset mode (R/W)

3. **Register 25.10. TWAI_DATA_5_REG (0x0054)**
   
4. **TWAI_TX_BYTE_5**
   - Description: Stored the 5th byte information of the data to be transmitted under operating mode (WO)
   - Binary Representation: `0 0 0 0 0 0 0 0`
   - Mask Value in Red Text on Right Side of Field: `[TWAI_ACCEPTANCE_MASK_1]`
   - Reset Value in Blue Text at Bottom Left of Field: `Reset`

5. **TWAI ACCEPTANCE MASK_1**
   - Description: Stored the 1st byte of the filter code under reset mode (R/W)

**Footer Information:** 
- "Espressif Systems"
- Page Number and Document Version:
  - "554 ESP32 TRM (Version 5.6)"
- Links for Submitting Documentation Feedback
  - `Submit Documentation Feedback`