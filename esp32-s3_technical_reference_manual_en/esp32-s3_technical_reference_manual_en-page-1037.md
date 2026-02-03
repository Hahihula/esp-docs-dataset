**Title:**
Chapter 27 I2C Controller (I2C)

**Subtitles and Body Texts with Descriptions of Registers:**

1. **Register 27.33, I2C_COMMD7_REG (0x0074)**
   - **Field Description:** 
     - `I2C_COMMAND7` is the content of command register 7.
     - It has a width similar to that in `I2C_COMMANDO`.
   - **Register Name and Access Type:**
     - I2C_COMMAND7 (R/W)

2. **Register 27.34, I2C_DATE_REG (0x00F8)**
   - **Field Description:** 
     - This is the version control register.
   - **Register Name and Access Type:**
     - I2C_DATE (R/W)
   
**Additional Information at Bottom of Page:**
- Company Logo/Name:
  - Espressif Systems
- Document Version Number:
  - ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
- Submit Documentation Feedback

**Diagrams and Descriptions in the Image:**

- **Diagram for I2C_COMMAND7:**
  - A binary representation of a register with bits labeled from `31` to `0`.
  - The label "Reset" is associated with bit `0`.

- **Diagram for I2C_DATE:**
  - Similar format as above, showing the same range and labeling.
  - The value `0x20070201` appears in one of the bits.

**Hyperlink Texts/Links at Bottom Right Corner:** 
- GoBack

(Note: There is no actual hyperlink text provided for "GoBack" which seems to be a clickable link or button.)