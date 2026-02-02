**Title:**
Chapter 22 I2S Controller (I2S)

**Menu:**
GoBack

**Section Title and Description:**

- **Register 22.26. I2S_LC_STATE1_REG (0x0070)**
  - Address: `0x00000000`
  - Description:
    ```
    I2S_LC_STATE1_REG
    Transmitter DMA channel status register.
    (RO)
    ```

- **Register 22.27. I2S_LC_HUNG_CONF_REG (0x0074)**
  - Address: `0x00000000`
  - Description:
    ```
    I2S_LC_HUNG_CONF_REG
    Transmitter DMA channel status register.
    (RO)
    ```

**Bit Fields and Descriptions for Register 22.27:**

- **I2S_LC_FIFO_TIMEOUT_ENA**
  - Access Type: Read/Write (`R/W`)
  - Description:
    ```
    The enable bit for FIFO timeout.
    ```

- **I2S_LC_FIFO_TIMEOUT_SHIFT**
  - Access Type: Read/Write (`R/W`)
  - Description:
    ```
    The bits are used to set the tick counter threshold. 
    The tick counter is reset when the count value >= 88000/2^12s LC fifo_timeout_shift.
    ```

- **I2S_LC_FIFO_TIMEOUT**
  - Access Type: Read/Write (`R/W`)
  - Description:
    ```
    When the value of FIFO hung counter is equal to this bit value, 
    sending data-timeout interrupt or receiving data-timeout interrupt will be triggered. 
    ``` 

**Footer Information:**

- Page Number: `444`
- Company Name and Document Version: "Espressif Systems ESP32 TRM (Version 5.6)"
- Link Texts:
  - Submit Documentation Feedback

**Diagram Description in the Image:**  
There is a diagram showing bit fields with labels such as `I2S_LC_FIFO_TIMEOUT_ENA`, `I2S_LC_HUNG_CONF_REG`, and others, but specific details about this are not provided. The bits range from positions 0 to 15 (0x001F). There's also a mention of "Reset" at position bit 7.

**Note:** 
The image contains technical information related to the I2S Controller in ESP32 and is likely part of an datasheet or reference manual.