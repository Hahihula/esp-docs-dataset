**Table:**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| PMS_CORE_X_IRAMO_PMS CONSTRAIN_1_REG | IBUS Permission Config Register 1 | 0x0ODC | R/W |
| PMS_CORE_X_IRAMO_PMS CONSTRAIN_2_REG | IBUS Permission Config Register 2 | 0x0OE0 | R/W |
| PMS_CORE_O_IRAMO_PMS_MONITOR_0_REG | CPUO IBUS Permission Interrupt Register 0 | 0x0E4 | R/W |
| PMS_CORE_O_IRAMO_PMS_MONITOR_1_REG | CPUO IBUS Permission Interrupt Register 1 | 0x0E8 | R/W |
| PMS_CORE_X_DRAMO_PMS CONSTRAIN_0_REG | DBUS Permission Config Register 0 | 0x0FC | R/W |
| PMS_CORE_X_DRAMO_PMS CONSTRAIN_1_REG | DBUS Permission Config Register 1 | 0x0100 | R/W |
| PMS_CORE_O_DRAMO_PMS_MONITOR_0_REG | CPUO dBUS Permission Interrupt Register 0 | 0x0104 | R/W |
| PMS_CORE_O_DRAMO_PMS_MONITOR_1_REG | CPUO dBUS Permission Interrupt Register 1 | 0x0108 | R/W |
| PMS_CORE_O_PIF_PMS CONSTRAIN_n_reg (n: 0 - 14) | Peripheral Permission Configuration Registers <br> 4*n | 0x124 + 4*n | R/W |
| PMS_CORE_O_REGION_PMS CONSTRAIN_0_REG | CPUO Split Region Permission Register 0 | 0x160 | R/W |
| PMS_CORE_O_REGION_PMS CONSTRAIN_1_REG | CPUO Split Region Permission Register 1 | 0x164 | R/W |
| PMS_CORE_O_REGION_PMS CONSTRAIN_2_REG | CPUO Split Region Permission Register 2 | 0x168 | R/W |
| PMS_CORE_O_REGION_PMS CONSTRAIN_3_REG | CPUO Split Region Permission Register 3 | 0x16C | R/W |
| PMS_CORE_O_PIF_PMS_MONITOR_0_REG | CPUO PIF Permission Interrupt Register 0 | 0x19C | R/W |
| PMS_CORE_O_PIF_PMS_MONITOR_1_REG | CPUO PIF Permission Interrupt Register 1 | 0x1A0 | R/W |
| PMS_CORE_O_PIF_PMS_MONITOR_4_REG | CPUO PIF Permission Interrupt Register 4 | 0x1AC | R/W |
| PMS CORE O VECBASE OVERRIDE_LOCK_REG | CPUO vecbase override configuration register 0 | 0x1B8 | R/W |
| PMS CORE O VECBASE OVERRIDE_0_REG | CPUO vecbase override configuration register 0 | 0x1BC | R/W |
| PMS CORE O VECBASE OVERRIDE_1_REG | CPUO vecbase override configuration register 1 | 0x1CO | R/W |
| PMS CORE O VECBASE OVERRIDE_2_REG | CPUO vecbase override configuration register 1 | 0x1C4 | R/W |
| PMS_EDMA_BOUNDARY_LOCK_REG | EDMA Boundary Lock Register | 0x2A8 | R/W |
| PMS_EDMABOUNDARY O REG | EDMA Boundary O Config Register | 0x2AC | R/W |
| PMS_EDMABOUNDARY_1 REG | EDMA Boundary 1 Config Register | 0x2B0 | R/W |
| PMS_EDMABOUNDARY_2 REG | EDMA Boundary 2 Config Register | 0x2B4 | R/W |
| PMS_EDMA_PMS_SPI2_LOCK_REG | SPI2 External Memory Permission Lock Register | 0x2B8 | R/W |
| PMS_EDMA_PMS_SPI2_REG | SPI2 External Memory Permission Config Register | 0x2BC | R/W |
| PMS_EDMA_PMS_SPI3_LOCK_REG | SPI3 External Memory Permission Lock Register | 0x2CO | R/W |

**Footer:**
- ESP32-S3 TRM (Version 1.7)