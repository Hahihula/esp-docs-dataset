**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Header:**
GoBack

**Register Information and Description:**

- **Register Name:** WCL_CORE_0_STATUSTABLE_CURRENT REG (0x00FC)
  - **Description:** Indicates the entry where the interrupt is currently at for CPUO. (R/W)
  - **Bitfield Diagram:**
    ```
    +-------------+-------------+
    |   31        |     16      |
    +-------------+-------------+
    |  reserved   | WCL_CORE_0_STATUSTABLE_CURRENT |
    +-------------+-------------+
    ```

- **Register Name:** Register 16.8, WCL_CORE_0_World_TRIGGER_ADDR REG (0x0140)
  - **Description:** Configures the entry address at which CPUO switches from Secure World to Non-secure World. (RW)
  - **Bitfield Diagram:**
    ```
    +-------------+-------------+
    |   31        |     0       |
    +-------------+-------------+
    |  reserved   | WCL_CORE_0_World_TRIGGER_ADDR |
    +-------------+-------------+
    ```

- **Register Name:** Register 16.9, WCL_CORE_0_World_PREPARE REG (0x0144)
  - **Description:** Write 0x2 to this field to ready CPUO for world switch from Secure World to Non-secure World. This field is only used for debugging.(R/W)
  - **Bitfield Diagram:**
    ```
    +-------------+-------------+
    |   31        |     2       |
    +-------------+-------------+
    |  reserved   | WCL_CORE_0_World_PREPARE |
    +-------------+-------------+
    ```

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)