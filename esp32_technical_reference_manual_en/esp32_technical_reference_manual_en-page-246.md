**Chapter Title:**
Chapter 12 DPort Registers

**GoBack Link:** GoBack

---

**Section Header (with register address):**
Register 12.1. DPORT_PRO_BOOT_REMAP_CTRL_REG (0x000)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from left to right.
- Description below the binary:
  - "DPRT_PRO_BOOT_REMAP" Remap mode for PRO_CPU. (R/W)
  
**Section Header:** 
Register 12.2. DPORT_APP_BOOT_REMAP_CTRL_REG (0x004)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from left to right.
- Description below the binary:
  - "DPRT_APP_BOOT_REMAP" Remap mode for APP_CPU. (R/W)
  
**Section Header:** 
Register 12.3. DPORT_PERI_CLK_EN_REG (0x01C)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from left to right.
- Description below the binary:
  - "DPRT_PERI_EN_RSA" Set the bit to enable the clock of RSA module. Clear the bit to disable the clock of RSA module. (R/W)
  - "DPRT_PERI_EN_SHA" Set the bit to enable the clock of SHA module. Clear the bit to disable the clock of SHA module. (R/W)
  - "DPRT_PERI_EN_AES" Set the bit to enable the clock of AES module. Clear the bit to disable the clock of AES module. (R/W)

**Footer:**
Espressif Systems
246 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback