**Chapter Title:**
Chapter 8 Chip Boot Control

**Tables and Descriptions**

1. **Table 8.3-1. Control of ROM Messages Printing to UARTO**
   - Columns:
     - Register
     - eFuse^2
     - GPIO46
     - ROM Messages Printing to UARTO
   - Rows:
     | Boot Mode       | Download Boot Mode | SPI Boot Mode |
     |-----------------|--------------------|---------------|
     |                 | 0                  | 1             |
     |                 | x                  | Disabled      |
     | Download Boot Mode | O                  | Enabled       |
     | SPI Boot Mode   |                   |               |
     |                 |                    |               |

2. **Table 8.3-2. Control of ROM Messages Printing to USB Serial/JTAG controller**
   - Columns:
     - Register
     - eFuse_1^2
     - eFuse_2^3
     - eFuse_3^4
     - ROM Messages Printing to USB Serial/JTAG controller
   - Rows:
     | Boot Mode       | Download Boot Mode | SPI Boot Mode |
     |-----------------|--------------------|---------------|
     |                 | 0                  |               |
     |                 | x                  |               |
     | Download Boot Mode | O                  | Enabled       |
     | SPI Boot Mode   |                   |               |

**Text Descriptions:**
1. **Table Notes for Table 8.3-2:**
   - Note:
     - The value of RTC_CNTL_RTC_STORE4_REG[0] can be read and written any number of times, whereas eFuse can only be burned once.
     - Therefore, RTC_CNTL_RTC_STORE4_REG[0] can be used to temporarily disable ROM messages printing,
       while eFuse can be used to permanently disable ROM messages printing.

2. **Additional Text:**
   - "Printing to USB Serial/JTAG controller is controlled as described in the table below."
   - "In SPI Boot mode, eFuse_2 is EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE;"
   - "In Download Boot mode, eFuse_3 is EFUSE_DIS_DOWNOAD_MODE;"
   - "In SPI Boot mode, eFuse_3 is EFUSE_DIS_USB_PRINT."

**Section Title:**
8.4 VDD_SPI Voltage Control

**Body Text for Section 8.4:**
- GPIO45 is used to select the VDD_SPI power supply voltage at reset:
- Espressif Systems
- Submit Documentation Feedback