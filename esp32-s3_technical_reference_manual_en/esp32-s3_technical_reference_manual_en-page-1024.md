**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** GoBack

---

**Register Section Header:**

- **Register Name and Address:**
  - Register 27.14, I2C_FIFO_CONF_REG (0x0018)

**Binary Representation Table for Register 27.14:**
```
| Bits | Description |
|-------|-------------|
| 31    | ...         |
| 15-0  | ...         |
```

---

**Field Descriptions and Values in Binary Format (for I2C_FIFO_CONF_REG):**

- **I2C_RXFIFO_WM_THRHD**
  - The watermark threshold of RX FIFO in non-FIFO mode.
    - When `I2C_FIFO_PRT_EN` is 1, the RX FIFO counter value must be greater than or equal to `I2C_RXFIFO_WM_THRHD[4:0]`.
    - When `I2C_RXFIFO_WM_INT_RAW` bit is valid. (Read/Write)

- **I2C_TXFIFO_WM_THRHD**
  - The watermark threshold of TX FIFO in non-FIFO mode.
    - When `I2C_FIFO_PRT_EN` is set to 1, the TX FIFO counter value must be smaller than or equal to `I2C_TXFIFO_WM_THRHD[4:0]`.
    - When `I2C_TXFIFO_WM_INT_RAW` bit is valid. (Read/Write)

- **I2C_NONFIFO_EN**
  - Set this bit to enable APB non-FIFO mode.
    - Valid for Read/Write.

- **I2C_FIFO_ADDR_CFG_EN**
  - When set, the byte received after I2C address represents offset and address in I2C Slave RAM. (Read/Write)

- **I2C_RX_FIFO_RST**
  - Set this bit to reset RX FIFO.
    - Valid for Read/Write.

- **I2C_TX_FIFO_RST**
  - Set this bit to reset TX FIFO.
    - Valid for Read/Write

- **I2C_FIFO_PRT_EN**
  - The control enable of FIFO pointer in non-FIFO mode. This controls valid bits and TX/RX FIFO overflow, underflow, full and empty interrupts.

---

**Register Section Header:**

- **Register Name and Address:**
  - Register 27.15, I2C_FILTER_CFG_REG (0x0050)

**Binary Representation Table for Register 27.15:**
```
| Bits | Description |
|-------|-------------|
| 31    | ...         |
| 10-0  | ...         |
```

---

**Field Descriptions and Values in Binary Format (for I2C_FILTER_CFG_REG):**

- **I2C_SCL_FILTER_THRES**
  - When a pulse on the SCL input has smaller width than `I2C_SCL_FILTER_THRES` field value, the controller ignores that pulse. (Read/Write)

- **I2C_SDA_FILTER_THRES**
  - When a pulse on the SDA input is shorter in duration compared to this threshold (`I2C_SDA_FILTER_THRES`), it's ignored by I2C module clock cycles.
    - Valid for Read/Write

- **I2C_SCL_FILTER_EN**
  - This bit enables filtering of SCL pulses. (Read/Write)

- **I2C_SDA_FILTER_EN**
  - This bit is the enable filter control signal for SDA input.

---

**Footer:**

Espressif Systems
1024 Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)