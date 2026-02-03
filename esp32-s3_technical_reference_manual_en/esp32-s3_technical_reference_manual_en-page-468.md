**Chapter Title:**
Chapter 5 eFuse Controller

**GoBack Link:** (Located at top right corner)

---

**Register Section Header and Description:**

- **Register Name**: Register 5.108, EFUSE_WR_TIME_CONF1_REG (0x01F4)
  - **Description**: Configures the power up time for VDDQ.
  - **Access Type**: Read/Write
  - **Address in Memory**: 0x2880

- **Register Name**: Register 5.109, EFUSE_WR_TIM_CONF2_REG (0x01F8)
  - **Description**: Configures the power off time for VDDQ.
  - **Access Type**: Read/Write
  - **Address in Memory**: 0x190

- **Register Name**: Register 5.110, EFUSE_STATUS_REG (0x01D0)
  - **Description**:
    - `EFUSE_REPEAT_ERR_CNT`: Represents the number of error bits during programming BLOCKO.
    - `EFUSE_STATE`: Represents the state of the eFuse state machine.

---

**Footer Information:**
- Page Number: 468
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name and Link**: Espressif Systems, Submit Documentation Feedback

--- 

**Binary Representation Examples for Registers:**

- **EFUSE_WR_TIME_CONF1_REG Example**:
  - Binary Layout with Reserved Bits Indicated
  - Hexadecimal Value when all bits are set to zero (0x2880)

- **EFUSE_WR_TIM_CONF2_REG Example**:
  - Binary Layout with Reserved Bits Indicated

- **EFUSE_STATUS_REG Example**:
  - Binary Layout: 
    - `EFUSE_REPEAT_ERR_CNT` and `EFUSE_STATE`
  - Hexadecimal Value when all bits are set to zero (0x0)

---

**Reset Information**: Each register has a reset value indicated in the binary layout. For example, for EFUSE_WR_TIME_CONF1_REG it is shown as "Reset" with specific bit positions highlighted.

(Note: The exact values and layouts of each field within registers 5.108 to 5.110 are not fully detailed here due to space constraints.)