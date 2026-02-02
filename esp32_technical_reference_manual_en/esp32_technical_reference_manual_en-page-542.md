**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Heading and Subsection with Content:**
- **DLC:** The Data Length Code (DLC) field specifies the number of data bytes for a Data Frame, or the number of data bytes to request in a Remote Frame. TWAI Data Frames are limited to a maximum payload of 8 data bytes, thus the DLC should range anywhere from 0 to 8.
- **X:** Don't care, can be any value.

**Subsection Title:**
25.5.4.3 Frame Identifier

**Body Text with Explanation and Reference Table:**
The Frame Identifier fields is 2 bytes (11-bits) if the message is SFF, and 4 bytes (29-bits) if the message is EFF.
The Frame Identifier fields for an SFF (11-bits) message shown in Table **25.5-5-25.5-6**.

**Table Titles:**
- Table 25.5-5. TX/RX Identifier 1 (SFF); TWAI Address Codes
- Table 25.5-6. TX/RX Identifier 2 (SFF); TWAI Address Codes

**Tables with Content and Structure:** 
Each table contains columns labeled as Bit positions from "Bit 31-8" to "Bit O". Specific bits are assigned values or reserved, such as ID numbers for SFF messages.

**Additional Subsection Title:**
25.5.7 TX/RX Identifier (EFF); TWAI Address Codes

**Table Titles and Content Continuation:** 
- Table 25.5-8. TX/RX Identifier 2 (EFF); TWAI Address Codes
- Table 25.5-9. TX/RX Identifier 3 (EFF); TWAI Address Codes
- Table 25.5-10. TX/RX Identifier 4 (EFF); TWAI Address Codes

**Tables with Content and Structure:** 
Each table contains columns labeled as Bit positions from "Bit 31-8" to "Bit O". Specific bits are assigned values or reserved, such as ID numbers for EFF messages.

**Footer:**
Espressif Systems
Submit Documentation Feedback
ESP32 TRM (Version 5.6)