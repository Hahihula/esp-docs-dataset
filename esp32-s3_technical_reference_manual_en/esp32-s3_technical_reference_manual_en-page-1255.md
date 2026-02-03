**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Section Heading:**
33.5 Register Summary

**Body Text:**
The addresses in this section are relative to USB Serial/JTAG Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table Headers (Column Titles):**
- Name
- Description
- Address
- Access

**Table Content:**

1. **Configuration Registers**
   - USB_SERIAL_JTAG_EP1_REG: Endpoint 1 FIFO register, Address: 0x0000, Access: R/W
   - USB_SERIAL_JTAG_EP1_CONF_REG: Endpoint 1 configure and status register, Address: 0x0004, Access: varies
   - USB_SERIAL_JTAG_CONFO_REG: Configure O register, Address: 0x0018, Access: R/W
   - USB_SERIAL_JTAG_MISC_CONF_REG: MISC register, Address: 0x0044, Access: R/W
   - USB_SERIAL_JTAG_MEM_CONF_REG: Memory power control, Address: 0x0048, Access: R/W
   - USB_SERIAL_JTAG_TEST_REG: USB Internal PHY test register, Address: 0x001C, Access: varies

2. **Interrupt Registers**
   - USB_SERIAL_JTAG_INT_RAW_REG: Raw status interrupt, Address: 0x0008, Access: R/WTC/SS
   - USB_SERIAL_JTAG_INT_ST_REG: Masked interrupt, Address: 0x000C, Access: RO
   - USB_SERIAL_JTAG_INT_ENA_REG: Interrupt enable bits, Address: 0x0010, Access: R/W
   - USB_SERIAL_JTAG_INT_CLR_REG: Interrupt clear bits, Address: 0x0014, Access: WT

3. **Status Registers**
   - USB_SERIAL_JTAG_JFIFO_ST_REG: USB-JTAG FIFO status, Address: 0x0020, Access: varies
   - USB_SERIAL_JTAG_FRAM_NUM_REG: SOF frame number, Address: 0x0024, Access: RO
   - USB_SERIAL_JTAG_IN_EPO_ST_REG: IN Endpoint O status, Address: 0x0028, Access: RO
   - USB_SERIAL_JTAG_IN_EP1_ST_REG: IN Endpoint 1 status, Address: 0x002C, Access: RO
   - USB_SERIAL_JTAG_IN_EP2_ST_REG: IN Endpoint 2 status, Address: 0x0030, Access: RO
   - USB_SERIAL_JTAG_IN_EP3_ST_REG: IN Endpoint 3 status, Address: 0x0034, Access: RO
   - USB_SERIAL_JTAG_OUT_EPO_ST_REG: OUT Endpoint O status, Address: 0x0038, Access: RO
   - USB_SERIAL_JTAG_OUT_EP1_ST_REG: OUT Endpoint 1 status, Address: 0x003C, Access: RO
   - USB_SERIAL_JTAG_OUT_EP2_ST_REG: OUT Endpoint 2 status, Address: 0x0040, Access: RO

4. **Version Register**
   - USB_SERIAL_JTAG_DATE_REG: Version control register, Address: 0x0080, Access: R/W

**Footer Information (Company and Document Details):**
Espressif Systems
1255 ESP32-S3 TRM (Version 1.7)

**Link Texts at the Bottom of Page:**
Submit Documentation Feedback