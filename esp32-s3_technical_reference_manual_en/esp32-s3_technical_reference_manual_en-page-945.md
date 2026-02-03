**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
26.6.2 UHCI Register Summary

**Body Text with Table:**

The addresses in this section are relative to UHCI Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section A Type Types for Registers.

**Table Headers (Column Titles):**
- Name
- Description
- Address
- Access

**Table Content:**

1. **Configuration Register**
   - UART_AT_CMD_PRECNT_REG
     - Pre-sequence timing configuration
     - 0x0050
     - R/W
   - UART_AT_CMD_POSTCNT_REG
     - Post-sequence timing configuration
     - 0x0054
     - R/W
   - UART_AT_CMD_GAPOUT_REG
     - Timeout configuration
     - 0x0058
     - R/W
   - UART_AT_CMD_CHAR_REG
     - AT escape sequence detection configuration
     - 0x005C
     - R/W

2. **Version Register**
   - UART_DATE_REG
     - UART version control register
     - 0x007C
     - R/W
   - UART_ID_REG
     - UART ID register
     - 0x0080
     - varies

**Configuration Register Section:**

- UHCI_CONFO_REG
  - UHCI configuration register
  - Address: 0x0000
  - Access: R/W
  
- Other registers continue in similar format, listing addresses and access types for various configuration settings.

**UHCI Interrupt Register**
- UHCI_INT_RAW_REG
  - Raw interrupt status
  - Address: varies

**Footer Information:**
Espressif Systems  
945 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback