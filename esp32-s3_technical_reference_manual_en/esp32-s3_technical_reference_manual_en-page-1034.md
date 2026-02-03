**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** GoBack

---

**Section Header:**
Register 27.25. I2C_INT_STATUS_REG (0x002C)

**Continuation Note:**
Continued from the previous page...

**List of Interrupt Status Bits for Register 27.25, I2C_INT_STATUS_REG (0x002C):**

- **I2C_SCL_ST_TO_INT_ST:** The masked interrupt status bit for the I2C_SCL_ST_TO_INT interrupt.
  - **Access Type:** Read Only
- **I2C_SCL_MAIN_ST_TO_INT_ST:** The masked interrupt status bit for the I2C_SCL_MAIN_ST_TO_INT interrupt.
  - **Access Type:** Read Only
- **I2C_DET_START_INT_ST:** The masked interrupt status bit for the I2C_DET_START_INT interrupt.
  - **Access Type:** Read Only
- **I2C_SLAVE_STRETCH_INT_ST:** The masked interrupt status bit for the I2C_SLAVE_STRETCH_INT interrupt.
  - **Access Type:** Read Only
- **I2C_GENERAL_CALL_INT_ST:** The masked interrupt status bit for the I2C_GENERAL_CALL_INT interrupt.
  - **Access Type:** Read Only

**Section Header:**
Register 27.26. I2C_COMDO_REG (0x0058)

**Diagram Description and Explanation of Bits in Register 27.26, I2C_COMDO_REG (0x0058):**

- **I2C_COMMANDO:** This is the content of command register O.
  - It consists of three parts:
    - op_code is the command: 
      - 1: WRITE
      - 2: STOP
      - 3: READ
      - 4: END
      - 6: RSTART
    - Byte_num represents the number of bytes that need to be sent or received.
    - ack_check_en, aack_exp and aack are used to control the ACK bit. For more information,
      see Section **27.4.9**.

- **Access Type:** Read/Write

- **I2C_COMMANDO_DONE:** When command 0 has been executed in master mode, this bit changes
  - To high level.
  - Access type: Read/Write (R/W/SS)

---

**Footer Information:**
Espressif Systems  
1034  
ESP32-S3 TRM (Version 1.7)  

**Links:** Submit Documentation Feedback