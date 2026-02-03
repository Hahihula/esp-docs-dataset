**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Heading:**
16.7 Register Summary

**Body Text:**

The addresses in this section are relative to the World Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

Note that, the table below only lists the registers for CPUO. CPU shares exactly the same set of registers.
Adding 0x0400 to the offset of the equivalent of CPUO register gives you address for CPU1 registers.

For example, the offset for CPUO register WCL_CORE_O ENTRY_CHECK_REG is Ox007C, the offset for CPU1 equivalent WCL CORE_1 ENTRY CHECK_REG should be Ox007C + 0x0400, which is Ox047C.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table:**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| Non-secure World to Secure World Configuration Registers | | | |
| WCL CORE O ENTRY n ADDR REG (n: 1-13) | CPUO Entry n Address Configuration Register | Ox0000 + 4\*(n - 1) | R/W |
| WCL CORE O ENTRY CHECK REG | CPUO Entry Check Enable Register | Ox007C | R/W |
| WCL CORE O MESSAGE ADDR REG | CPUO Clear Writer buffer Configuration Register - Configures Address | Ox0100 | R/W |
| WCL CORE O MESSAGE MAX REG | CPUO Clear Writer buffer Configuration Register - Configures sequence | Ox0104 | R/W |
| WCL CORE O MESSAGE PHASE REG | CPUO Clear Writer buffer Configuration Register - Checks Status | Ox0108 | RO |
| Status Table Registers | | | |
| WCL CORE O STATABLEn REG (n: 1-13) n | CPUO World Switch Status Register for Entry + 4\*(n - 1) | Ox0080 R/W |
| WCL CORE O STATABLE CURRENT REG | CPUO Status Register of Statutable Current Field | Ox00FC R/W |
| Secure World to Non-secure World Configuration Registers | | | |
| WCL CORE O World TRIGGER ADDR REG | CPUO Trigger Address Configuration Register | Ox0140 RW | - |
| WCL CORE O World PREPARE REG | CPUO World Configuration Register - Configures Entry Addresses | Ox0144 R/W | - |
| WCL CORE O World UPDATE REG | CPUO World Configuration Register - Confirms Configuration Done | Ox0148 WO | - |
| WCL CORE O World Cancel REG | CPUO World Configuration Register - Cancels Configuration | Ox014C WO | - |
| WCL CORE O World IRam0 REG | CPUO IRAMO World Status Register | Ox0150 R/W | - |
| WCL CORE O World DRam0 PIF REG | CPUO Dramo and PIF World Status Register | Ox0154 R/W | - |
| WCL CORE O World Phase REG | CPUO World Status Register | Ox0158 RO | - |
| NMI Mask Configuration Registers | | | |
| WCL CORE O NMI MASK ENABLE REG | CPUO NMI Mask Enable Register | Ox0180 WO | - |
| WCL CORE O NMI MASK TRIGGER ADDR REG | CPUO NMI Mask Trigger Address Register | Ox0184 R/W | - |

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7) Page number at the bottom is "812"