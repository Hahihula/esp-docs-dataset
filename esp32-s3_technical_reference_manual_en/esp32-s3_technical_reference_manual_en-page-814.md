**Title:**
Chapter 16 World Controller (WCL)

**Subtitle:**
16.8 Registers

**Body Text:**

The addresses in this section are relative to the World Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

Note that, the section below only lists the registers for CPU0. CPU1 shares exactly the same set of registers. Adding 0x0400 to the offset of the equivalent of CPU0 register gives you address for CPU1 registers.
For example, the offset for CPU0 register WCL_CORE_0 ENTRY_CHECK_REG is 0x007C, the offset for CPU1 equivalent WCL CORE_1 ENTRY CHECK REG should be 0x007C + 0x0400, which is 0x047C.

**Image Descriptions:**

- **Figure Caption:** Register 16.1. WCL CORE O ENTRY n ADDR REG (n: 1-13) (0x0000+4*(n-1))
- The figure shows a register layout with fields labeled as "WCL CORE O ENTRY n ADDR" and an address range from '0' to '15'.

**Additional Information in Image:**

- **Figure Caption:** Register 16.2. WCL CORE_0 ENTRY_CHECK_REG (0x007C)
- The figure shows a register layout with fields labeled as "WCL CORE O ENTRY CHECK" and an address range from '0' to '15'.

**Text Descriptions:**

- **Description:** 
  - `WCL CORE_0 ENTRY n ADDR` Configures the CPUO Entry n address from Non-secure World to Secure World. (R/W)
  - `WCL CORE_0 ENTRY CHECK` Set this bit to enable CPUO switching from Non-secure World to Secure world upon the monitored address. (R/W)

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)