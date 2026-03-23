

# 15.6 Register Summary

The addresses in this section are relative to the World Controller base address provided in Table 3.3-3 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **WORLD1 to WORLD0 Configuration Registers** | | | |
| WCL_Core_O_MTVEC_BASE_REG | MTVEC configuration | 0x0000 | R/W |
| WCL_Core_O_MSTATUS_MIE_REG | MSTATUS_MIE configuration | 0x0004 | R/W |
| WCL_Core_O_ENTRY_CHECK_REG | CPU entry check configuration | 0x0008 | R/W |
| **StatusTable Registers** | | | |
| WCL_Core_O_STATUSTABLEN_REG (n: 0-31) | Entry n world switching status | 0x0040 | R/W |
| WCL_Core_O_STATUSTABLE_CURRENT_REG | Represents the entry where the interrupt is currently at | 0x00E0 | R/W |
| **WORLD0 to WORLD1 Configuration Registers** | | | |
| WCL_Core_O_World_TRIGGER_ADDR_REG | CPU trigger address configuration | 0x0140 | RW |
| WCL_Core_O_World_PREPARE_REG | CPU world switching preparation configuration | 0x0144 | R/W |
| WCL_Core_O_World_UPDATE_REG | CPU world switching update configuration | 0x0148 | WO |
| WCL_Core_O_World_Cancel_REG | CPU world switching cancel configuration | 0x014C | WO |
| WCL_Core_O_World_IRamO_REG | CPU IBUS world info | 0x0150 | R/W |
| WCL_Core_O_World_DRamO_PIF_REG | CPU DBUS and PIF bus world info | 0x0154 | R/W |
| WCL_Core_O_World_Phase_REG | CPU world switching readiness | 0x0158 | RO |