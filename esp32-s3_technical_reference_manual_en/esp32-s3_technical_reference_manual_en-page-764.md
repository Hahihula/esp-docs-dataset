**Title:**
Register 15.53. PMS_CORE_0_PIF_PMS CONSTRAINT_11_REG (0x0150)

**Diagram Labels and Values:**
- PMS_CORE_0_PIF_PMS CONSTRAINT_RTCSSLOW_0_SPLTADDR_WORLD_0
- PMS_CORE_0_PIF_PMS CONSTRAINT_RTCSSLOW_0_SPLTADDR_WORLD_1

**Table Description (Binary Table):**
```
+-------------+------------------+------------------+
| 31         |      22         |       21        |
+-------------+------------------+------------------+
|    0       |     0           |     0           |
+-------------+------------------+------------------+
|   0x7ff    |                 |                 |
+-------------+------------------+------------------+
```

**Text Descriptions:**
- **PMS_CORE_0_PIF_PMS CONSTRAINT_RTCSSLOW_0_SPLTADDR_WORLD_0**: Configures the address to split RTC Slow Memory O into two regions in Secure World for CPUO. Note you should use address offset, instead of absolute address. (R/W)
  
- **PMS_CORE_0_PIF_PMS CONSTRAINT_RTCSSLOW_0_SPLTADDR_WORLD_1**: Configures the address to split RTC Slow Memory 0 into two regions in Non-secure World for CPUO. Note you should use address offset, instead of absolute address. (R/W)

**Footer:**
ESP32-S3 TRM (Version 1.7)