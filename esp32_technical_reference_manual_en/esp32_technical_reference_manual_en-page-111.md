**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Section Header:**
GoBack

**Register Description and Details for EFUSE CONFIRMATION REGISTER**

- **Register Name:** Register 5.22.
- **Register Address:** EFUSE_CONF_REG (0x0fc)
- **Bit Description:**
  - **Name:** EFUSE_OP_CODE
  - **Description:** eFuse operation code register. (R/W)

**Bit Layout Diagram for EFUSE CONFIRMATION REGISTER**

```
+-------------+
|   31       |<reserved>|
+-------------+
|   16       |
|   15       |
|   ...      |
|   0        |
+-------------+
|  0x0000    |
| Reset      |
+-------------+
```

**Register Description and Details for EFUSE COMMAND REGISTER**

- **Register Name:** Register 5.23.
- **Register Address:** EFUSE_CMD_REG (0x104)
- **Bit Description:**
  - **Name:** EFUSE_PGM_CMD
  - **Description:** Set this to 1 to start a program operation. Reverts to 0 when the program operation is done. (R/W)

  - **Name:** EFUSE_READ_CMD
  - **Description:** Set this to 1 to start a read operation. Reverts to 0 when the read operation is done. (R/W)

**Bit Layout Diagram for EFUSE COMMAND REGISTER**

```
+-------------+
|   31       |
|   ...      |
|   2        |<reserved>|
|   1        |
|   0        |
+-------------+
| Reset      |
+-------------+
```

**Register Description and Details for EFUSE INTERRUPT RAW REGISTER**

- **Register Name:** Register 5.24.
- **Register Address:** EFUSE_INT_RAW_REG (0x108)
- **Bit Description:**
  - **Name:** EFUSE_PGM_DONE_INT_RAW
    - **Description:** The raw interrupt status bit for the EFUSE_PGMDoneInt interrupt. (RO)

  - **Name:** EFUSE_READ_DONE_INT_RAW
    - **Description:** The raw interrupt status bit for the EFUSEReadDoneInt interrupt. (RO)

**Bit Layout Diagram for EFUSE INTERRUPT RAW REGISTER**

```
+-------------+
|   31       |
|   ...      |
|   2        |<reserved>|
|   1        |
|   0        |
+-------------+
| Reset      |
+-------------+
```

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32 TRM (Version 5.6)