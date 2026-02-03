**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Section Heading and Subheading:**
17.5 Registers

**Body Text:**
In this section, the addresses of all the registers starting with SYSTEM are relative to the base address of system registers provided in Table 4.3-3 in Chapter 4 System and Memory; and those starting with APB are relative to the base address of APB control also provided in Table 4.3-3 in Chapter 4 System and Memory.

**Register Information:**
- **Register Name:** Register 17.1. SYSTEM_CORE_1_CONTROL_0_REG (0x0000)
  - **Diagram Description:**
    ```
    +-------+-------+-------+-------+
    |       |       |       |       |
    |   3   |   2   |   1   |   0   |
    +-------+-------+-------+-------+
    | SYSTEM_CONTROL CORE_1_RESETALL (reset) |
    | SYSTEM_CONTROL CORE_1_RUNSTALL Set this bit to stall Core 1. (R/W) |
    | SYSTEM_CONTROL CORE_1_CLKGATE_EN Set this bit to enable Core 1 clock. (R/W) |
    | SYSTEM_CONTROL CORE_1_RESETTING Set this bit to reset Core 1. (R/W) |
    +-------+-------+-------+-------+
    ```
- **Register Name:** Register 17.2. SYSTEM_CORE_1_CONTROL_1_REG (0x0004)
  - **Diagram Description:**
    ```
    +-------+-------+-------+-------+
    |       |       |       |       |
    |   3   |   2   |   1   |   0   |
    +-------+-------+-------+-------+
    | SYSTEM_CONTROL CORE_1_MESSAGE Sets the boot address for CPU1. Please note that this field is only effective during the first boot of CPU1; afterwards, users can configure it for other purposes as needed. (R/W) |
    +-------+-------+-------+-------+
    ```

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** ESP32-S3 TRM (Version 1.7)

**Navigation Link:**
GoBack