**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**GoBack**

**Subtitle:**
Register 33.10. USB_SERIAL_JTAG_TEST_REG (0x001C)

**Body Text with Binary Representation and Descriptions for Each Bit Field:**
- **0**: Reserved
- **1**: USB_SERIAL_JTAG_TEST_ENABLE - Enable test of the USB pad. (R/W)
- **2**: USB_SERIAL_JTAG_TEST_OE - USB pad oe in test. (R/W)
- **3**: USB_SERIAL_JTAG_TEST_TX_DP - USB D+ tx value in test. (R/W)
- **4**: USB_SERIAL_JTAG_TEST_TX_DM - USB D- tx value in test. (R/W)
- **5**: USB_SERIAL_JTAG_TEST_RX_RCV - USB differential rx value in test. (RO)
- **6**: USB_SERIAL_JTAG_TEST_RX_DP - USB D+ rx value in test. (RO)
- **7**: USB_SERIAL_JTAG_TEST_RX_DM - USB D- rx value in test. (RO)

**Subtitle:**
Register 33.11. USB_SERIAL_JTAG_FIFO_ST_REG (0x0020)

**Body Text with Binary Representation and Descriptions for Each Bit Field:**
- **0**: Reserved
- **1**: USB_SERIAL_JTAG_IN_FIFO_CNT - JTAT in fifo counter. (RO)
- **2**: USB_SERIAL_JTAG_IN_FIFO_EMPTY - 1: JTAG in fifo is empty. (RO)
- **3**: USB_SERIAL_JTAG_IN_FIFO_FULL - 1: JTAG in fifo is full. (RO)
- **4**: USB_SERIAL_JTAG_OUT_FIFO_CNT - JTAT out fifo counter. (RO)
- **5**: USB_SERIAL_JTAG_OUT_FIFO_EMPTY - 1: JTAT out fifo is empty. (RO)
- **6**: USB_SERIAL_JTAG_OUT_FIFO_FULL - 1: JTAT out fifo is full. (RO)
- **7**: USB_SERIAL_JTAG_IN_FIFO_RESET - Write 1 to reset JTAG in fifo. (R/W)
- **8**: USB_SERIAL_JTAG_OUT_FIFO_RESET - Write 1 to reset JTAT out fifo. (R/W)

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)