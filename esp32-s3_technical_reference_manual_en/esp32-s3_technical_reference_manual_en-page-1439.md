**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**GoBack Link:** GoBack

---

**Section Header: Register 3717. RMT_TX_SIM_REG (0x00C4)**

- **Field Description for RMT_TX_SIM_CHn**: 
  - **Description**: Set this bit to enable channel \( n \) to start sending data simultaneously with other enabled channels.
  - **Register Access**: Read/Write
  - **Bit Range**: Not specified in the image.

- **Field Description for RMT_TX_SIM_EN**:
  - **Description**: This bit is used to enable multiple channels to start sending data simultaneously.
  - **Register Access**: Read/Write

---

**Section Header: Register 3718. RMT_CHm_RX_LIM_REG ( \( m = 4, 5, 6, 7 \) )**

- **Field Description for RMT_CHm_RX_LIM_REG**:
  - **Description**: This field is used to configure the maximum entries that channel \( m \) can receive.
  - **Register Access**: Read/Write

---

**Section Header: Register 3719. RMT_DATE_REG (0x00CC)**

- **Field Description for RMT_DATE**:
  - **Description**: Version control register.

---

**Footer Information:** 
- Page Number: 1439
- Company Name: Espressif Systems
- Document Title: ESP32-S3 TRM (Version 1.7)
- Link Texts: Submit Documentation Feedback

(Note: The image contains binary representations and reset indicators for each register, but these are not transcribed as text.)