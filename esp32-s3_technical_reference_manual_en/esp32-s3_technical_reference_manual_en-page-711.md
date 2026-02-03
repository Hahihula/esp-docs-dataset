**Title:**
15.10 Registers

**Body Text:**
The addresses of registers starting from PMS in this section are relative to the Permission Control base address, and the addresses of registers starting from APB in this section are relative to the ABP Controller base address. Both base address are provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subtitle:**
Register 15.1. PMS_APB_PERIPHERAL_ACCESS_0_REG (0x008)

**Diagram Description:**
A diagram showing a register layout with bits labeled from 'reserved' to the end, indicating bit positions for different functions within the register.
- The label "PMS_APB_PERIPHERAL_ACCESS_LOCK" is associated with one of the bits in this section.

**Additional Information on Diagram:**
PMS_APB Peripheral Access Lock
Set this bit to lock APB peripheral configuration register. (R/W)

**Footer Text:**
ESP32-S3 TRM (Version 1.7)