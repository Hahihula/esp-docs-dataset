**Title:**
Chapter 12 Timer Group (TIMG)

**Header:**
Register 12.26. TIMG_REGCLK_REG (0x00FC)

**Binary Diagram Description:**
- The diagram shows a binary representation of the register with bits labeled from '31' to '0'.
- Each bit is represented by either '1' or '0'.

**Text Explanation for Register:**
TIMG_CLK_EN
- **Description:** Register clock gate signal.
- **Value 0 (Software Clock):** The clock used by software to read and write registers is on only when there is software operation. 
- **Value 1 (Always On):** The clock used by software to read and write registers is always on.

**Footer:**
Espressif Systems
671 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Navigation Link:**
GoBack