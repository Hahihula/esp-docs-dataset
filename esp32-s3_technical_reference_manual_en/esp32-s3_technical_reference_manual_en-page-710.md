**Table: CPU Permission Control (PMS)**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| PMS_CORE_O_DRAMO_PMS_MONITOR_3_REG | CPU0 dBUS Permission Interrupt Register 3 | 0x0110 | RO |
| PMS_CORE_O_PIF_PMS_MONITOR_2_REG | CPU0 PIF Permission Interrupt Register 2 | 0x01A4 | RO |
| PMS_CORE_O_PIF_PMS_MONITOR_3_REG | CPU0 PIF Permission Interrupt Register 3 | 0x01A8 | RO |
| PMS_CORE_O_PIF_PMS_MONITOR_5_REG | CPU0 PIF Permission Interrupt Register 5 | 0x01B0 | RO |
| PMS_CORE_O_PIF_PMS_MONITOR_6_REG | CPU0 PIF Permission Interrupt Register 6 | 0x01B4 | RO |

**Version Register**

- **PMS_DATE_REG**: Sensitive Version Register
- Address: 0xFFC
- Access: R/W

---

**Configuration Registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| SYSCON_EXT_MEM_PMS_LOCK_REG | External Memory Permission Lock Register | 0x020 | R/W |
| SYSCON_FLASH_ACEn ATTR_REG (n: 0 - 3) | Flash Area n Permission Config Register | 0x028 + 4*n | R/W |
| SYSCON_SRAM_ACEn ADDR_S (n: 0 - 3) | Flash Area s Starting Address Config Register | 0x038 + 4*n | R/W |
| SYSCON_FLASH_ACEn SIZE_REG (n: 0 - 3) | Flash Area n Length Config Register | 0x048 + 4*n | R/W |
| SYSCON_SRAM_ACEn ATTR_REG (n: 0 - 3) | External SRAM Area n Permission Config Register | 0x058 + 4*n | R/W |
| SYSCON_SRAM_ACEn ADDR_REG (n: 0 - 3) | External SRAM Area n Starting Address Config Register | 0x068 + 4*n | R/W |
| SYSCON_SRAM_ACEn SIZE_REG (n: 0 - 3) | External SRAM Area s Length Config Register | 0x078 + 4*n | R/W |
| SYSCON_SPI_MEM_PMS_CTRL_REG | External Memory Unauthorized Access Interrupt Register | varies | varies |
| SYSCON_SRAM_MEM_REJECT_ADDR_REG | External Memory Unauthorized Access Address Register | 0x08C | RO |

---

*Note: The table includes specific addresses and access permissions for various registers related to CPU permission control, memory configuration settings, and external memory management.*