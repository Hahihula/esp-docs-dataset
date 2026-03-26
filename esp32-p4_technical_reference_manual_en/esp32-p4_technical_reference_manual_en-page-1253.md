

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| HP_SYSTEM_AHB2AXI_BRESP_ERR_INT_ENA_REG   | AHB to AXI BRESP error interrupt enable                                    | 0x0190    | R/W    |
| HP_SYSTEM_AHB2AXI_BRESP_ERR_INT_CLR_REG   | AHB to AXI BRESP error interrupt clear                                      | 0x0194    | WT     |
| HP_SYSTEM_L2_MEM_L2_RAM_ECC_REG           | HP L2MEM ECC enable                                                         | 0x00AC    | R/W    |
| HP_SYSTEM_L2_MEM_INT_RECORD0_REG          | HP L2MEM interrupt record 0                                                 | 0x00BO    | RO     |
| HP_SYSTEM_L2_MEM_INT_RECORD1_REG          | HP L2MEM interrupt record 1                                                 | 0x00B4    | RO     |
| HP_SYSTEM_L2_MEM_L2_CACHE_ECC_REG         | L2 cache ECC enable                                                         | 0x00C4    | R/W    |
| HP_SYSTEM_HP_L1CACHE_BUS0_ID_REG          | L1 cache bus O ID                                                           | 0x00C8    | R/W    |
| HP_SYSTEM_HP_L1CACHE_BUS1_ID_REG          | L1 cache bus 1 ID                                                           | 0x00CC    | R/W    |
| HP_SYSTEM_GPIO_DED_HOLD_CTRL_REG          | HP GPIO hold control                                                        | 0x00F0    | R/W    |
| HP_SYSTEM_HP_USB2OOTG_MEM_CTRL_REG        | MEM in USB OTG FS clock force on                                            | 0x00F8    | R/W    |
| HP_SYSTEM_HP_SPM_PARITY_INT_RECORD_REG    | HP SPM parity interrupt status                                              | 0x010C    | RO     |
| HP_SYSTEM_HP_L1_CACHE_PWR_CTRL_REG        | HP L1 cache memory force on                                                | 0x0110    | R/W    |
| HP_SYSTEM_HP_L2_CACHE_PWR_CTRL_REG        | HP L2 cache memory force on                                                | 0x0114    | R/W    |
| HP_SYSTEM_HP_CPU_WAITI_CONF_REG           | CPU_WAITI configuration                                                     | 0x0118    | R/W    |
| HP_SYSTEM_CORE_DEBUG_UNSTALL_CONF_REG     | CPU debug runstall configuration                                            | 0x011C    | R/W    |
| HP_SYSTEM_HP_CORE_AHB_TIMEOUT_REG         | HP CPU AHB bus timeout                                                      | 0x0120    | R/W    |
| HP_SYSTEM_HP_CORE_IBUS_TIMEOUT_REG        | HP CPU IBUS timeout                                                         | 0x0124    | R/W    |
| HP_SYSTEM_HP_CORE_DBUS_TIMEOUT_REG        | HP CPU DBUS timeout                                                         | 0x0128    | R/W    |
| HP_SYSTEM_HP_ICM_CPU_H2X_CFG_REG          | AHB to AXI bridge configuration                                             | 0x0138    | varies |
| HP_SYSTEM_PERI1_APB_POSTW_EN_REG          | HP PERI1 APB post write enable                                              | 0x013C    | R/W    |
| HP_SYSTEM_BITSCRAMBLER_PERI_SEL_REG       | BitScrambler peripherals select                                             | 0x0140    | R/W    |
| HP_SYSTEM_APB_SYNC_POSTW_EN_REG           | HP PREIO APB post write enable                                              | 0x0144    | R/W    |
| HP_SYSTEM_HP_RSA_PD_CTRL_REG               | RSA memory PD control                                                       | 0x01D0    | R/W    |
| HP_SYSTEM_HP_ECC_PD_CTRL_REG               | ECC memory PD control                                                       | 0x01D4    | R/W    |
| HP_SYSTEM_HP_RNG_CFG_REG                  | RNG configuration                                                           | 0x01D8    | varies |
| HP_SYSTEM_HP_UART_PD_CTRL_REG             | Memory PD control                                                           | 0x01DC    | R/W    |
| HP_SYSTEM_HP_PERI_MEM_CLK_FORCE_ON_REG    | HP PERI memory clock force on                                               | 0x01E0    | R/W    |
| HP_SYSTEM_GDMA_CTRL_REG                   | DW-GDMA control                                                             | 0x0148    | R/W    |
| HP_SYSTEM_GMAC_CTRL0_REG                  | GMAC control 0                                                              | 0x014C    | varies |
| HP_SYSTEM_GMAC_CTRL1_REG                  | GMAC control 1                                                              | 0x0150    | RO     |
| HP_SYSTEM_GMAC_CTRL2_REG                  | GMAC control 2                                                              | 0x0154    | RO     |
| HP_SYSTEM_USBOTG20_CTRL_REG               | USB OTGHS control                                                           | 0x015C    | varies |
| HP_SYSTEM_HP_SPM_ERR_RESP_CTRL_REG        | HP SPM error response enable                                                | 0x0160    | R/W    |
| HP_SYSTEM_L2_MEM_REFRESH_REG              | HP SPM refresh                                                              | 0x0164    | varies |
| HP_SYSTEM_HP_SPM_INIT_REG                 | HP SPM initialization                                                       | 0x0168    | varies |
| HP_SYSTEM_HP_SPM_PARITY_CHECK_CTRL_REG    | HP SPM parity check enable                                                  | 0x016C    | R/W    |
| HP_SYSTEM_L2_MEM_ERR_RESP_CTRL_REG        | HP L2MEM error response                                                     | 0x0198    | R/W    |
| HP_SYSTEM_L2_MEM_AHB_BUFFER_CTRL_REG      | HP L2MEM AHB buffer enable                                                  | 0x019C    | R/W    |
| HP_SYSTEM_HP_CORE_DMACTIVE_LPCORE_REG     | HP CPU debug module active                                                  | 0x01A0    | RO     |

**Control Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| HP_SYSTEM_HP_CORE_ERR_RESP_DIS_REG        | HP CPU error response masked                                                | 0x01A4    | R/W    |
| HP_SYSTEM_GPIO_O_HYS_CTRL0_REG            | HP GPIO hold control 0                                                     | 0x01C0    | R/W    |
```