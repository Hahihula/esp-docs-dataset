**Title:**
Chapter 15 Permission Control (PMS)

**Note Section:**
- Registers PMS_CORE_0_PIF_PMSCONSTRAIN_n_REG (n: 1 - 4) are for configuring the CPUO's permission to different peripherals from the Secure World.
- Registers PMS_CORE_0_PIF_PMSCONSTRAIN_n_REG (n: 5 - 8) are for configuring the CPUO's permission to different peripherals from the Non-secure World.

**Additional Information:**
Detailed information are already provided in Table 15.4-1. For brevity, these registers are not described separately in this section.

**Register Description (Register 15.51):**
PMS_CORE_0_PIF_PMSCONSTRAIN_9_REG (0x0148)

**Diagram:**
A diagram showing the layout of PMS CORE_0 PIF PMS CONSTRAIN_9_REG with labels indicating different sections and their corresponding bit positions.

**Description for Specific Registers within Diagram:**
- **PMS_CORE_0_PIF_PMSCONSTRAIN_RTCFAST_SPLTADDR_WORLD_0**: Configures the address to split RTC Fast Memory into two regions in Non-secure World for CPUO. Note you should use address offset, instead of absolute address. (R/W)
- **PMS_CORE_0_PIF_PMSCONSTRAIN_RTCFAST_SPLTADDR_WORLD_1**: Configures the address to split RTC Fast Memory into two regions in Secure World for CPUO. Note you should use address offset, instead of absolute address. (R/W)

**Footer:**
ESP32-S3 TRM (Version 1.7)