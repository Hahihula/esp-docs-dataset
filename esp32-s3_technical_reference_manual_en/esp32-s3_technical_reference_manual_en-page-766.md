**Title:**
Register 15.55. PMS_CORE_0_PIF_PMS CONSTRAINT_13_REG (0x0158)

**Diagram Labels and Descriptions:**
- PMS_CORE_0_PIF_PMS CONSTRAINT_RTSLOW_1 SPLTADDR_WORLD_0
- PMS_CORE_0_PIF_PMS CONSTRAINT_RTSLOW_1 SPLTADDR_WORLD_1

**Text Content with Descriptions of Register Settings:**

- **PMS_CORE_0_PIF_PMS CONSTRAINT_RTSLOW_1 SPLTADDR_WORLD_0**
  - Description:
    Configures the address to split RTC Slow Memory into two regions in Secure World for CPUO. Note you should use address offset, instead of absolute address.
  - Access Type: Read/Write (R/W)

- **PMS_CORE_0_PIF_PMS CONSTRAINT_RTSLOW_1 SPLTADDR_WORLD_1**
  - Description:
    Configures the address to split RTC Slow Memory into two regions in Non-secure World for CPUO. Note you should use address offset, instead of absolute address.
  - Access Type: Read/Write (R/W)

**Footer Information:**
ESP32-S3 TRM (Version 1.7)