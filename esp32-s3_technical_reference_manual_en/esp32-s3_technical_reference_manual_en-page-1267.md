**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**GoBack Link:** GoBack

---

**Register Section Header:**

- **Register Name and Address:**
  - Register 33.18, USB_SERIAL_JTAG_OUT_EP1_ST_REG (0x003C)
  
  **Bit Description Table for Register 33.18:**
  ```
  +-------------+------------------+-----------+
  | Bit Number  | Bit Name         | Access    |
  +-------------+------------------+-----------+
  |   31        |     reserved     |           |
  +-------------+------------------+-----------+
  |   23-0      | USB_SERIAL_JTAG_OUT_EP1Rec_Data_CNT | (RO) |
  +-------------+------------------+-----------+
  |    9        | USB_SERIAL_JTAG_OUT_EP1_WR_ADDR | (RO) |
  +-------------+------------------+-----------+
  |    8        | USB_SERIAL_JTAG_OUT_EP1_ST_REG | (RO) |
  +-------------+------------------+-----------+
  |    2-0      | USB_SERIAL_JTAG_OUT_EP1State | Reset |
  +-------------+------------------+-----------+
  ```

**Description for Register 33.18:**
- **Field Name:** USB_SERIAL_JTAG_OUT_EP1_STATE
- **Description:** State of OUT Endpoint 1 (RO)
- **Access Mode:** Read Only

**Details about the Fields in Register 33.18:**

- When `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` is detected, there are:
  - USB_SERIAL_JTAG_OUT_EP1_WR_ADDR-2 bytes data in OUT EP1.
  
- Data address of OUT endpoint 1.

---

**Register Section Header:**

- **Register Name and Address:**
  - Register 33.19, USB_SERIAL_JTAG_OUT_EP2_ST_REG (0x0040)
  
  **Bit Description Table for Register 33.19:**
  ```
  +-------------+------------------+-----------+
  | Bit Number  | Bit Name         | Access    |
  +-------------+------------------+-----------+
  |   31        |     reserved     |           |
  +-------------+------------------+-----------+
  |   23-0      | USB_SERIAL_JTAG_OUT_EP2Rec_Data_CNT | (RO) |
  +-------------+------------------+-----------+
  |    9        | USB_SERIAL_JTAG_OUT_EP2_WR_ADDR | (RO) |
  +-------------+------------------+-----------+
  |    8        | USB_SERIAL_JTAG_OUT_EP2_ST_REG | (RO) |
  +-------------+------------------+-----------+
  |    2-0      | USB_SERIAL_JTAG_OUT_EP2State | Reset |
  +-------------+------------------+-----------+
  ```

**Description for Register 33.19:**
- **Field Name:** USB_SERIAL_JTAG_OUT_EP2_STATE
- **Description:** State of OUT Endpoint 2 (RO)
- **Access Mode:** Read Only

**Details about the Fields in Register 33.19:**

- When `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` is detected, there are:
  - USB_SERIAL_JTAG_OUT_EP2_WR_ADDR-2 bytes data in OUT EP2.
  
- Data address of OUT endpoint 2.

---

**Footer Information:** 
Espressif Systems
Page Number: 1267
Document Version: ESP32-S3 TRM (Version 1.7)
Feedback Link: Submit Documentation Feedback