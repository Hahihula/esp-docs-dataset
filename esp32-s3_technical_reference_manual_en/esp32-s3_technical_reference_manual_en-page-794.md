**Title:**
Chapter 15 Permission Control (PMS)

**Register Information:**
- Register Name: PMS_CORE_0_PIF_PMS_MONITOR_5_REG (0x01B0)
- Description:
  - **Field:** PMS_CORE_0_PIF_PMS_MONITOR_NONWORD_VIOLATE_STATUS_HWORLD
    - Stores the interrupt status of PIF unsupported data type. (RO)
  - **Field:** PMS_CORE_0_PIF_PMS_MONITOR_NONWORD_VIOLATE_STATUS_HSIZE
    - Stores the data type when the unauthorized access happened. (RO)
  - **Field:** PMS_CORE_0_PIF_PMS_MONITOR_NONWORD_VIOLATE_STATUS_INTR
    - Stores the world the CPU was in when the unauthorized access happened.
      - 01: Secure World; 10: Non-secure World.

**Diagram Description:**
The diagram shows a bitfield layout for register PMS_CORE_0_PIF_PMS_MONITOR_5_REG. The fields are labeled as follows:
- **31:** (reserved)
- Other bits from 2 to 0 represent the various status indicators described above.
- There is also an indication of "Reset" at position [0].

**Footer:**
ESP32-S3 TRM (Version 1.7)