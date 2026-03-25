

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| PCR_SARADC_CLKMK_CONF_REG                 | SARADC_CLKMK configuration register                                        | 0x0078    | R/W    |
| PCR_TSENS_CLK_CONF_REG                    | TSENS_CLK configuration register                                           | 0x007C    | R/W    |
| PCR_USB_DEVICE_CONF_REG                   | USB_DEVICE configuration register                                          | 0x0080    | varies |
| PCR_INTMTX_CONF_REG                       | INTMTX configuration register                                              | 0x0084    | varies |
| PCR_GDMA_CONF_REG                         | GDMA configuration register                                                | 0x0090    | R/W    |
| PCR_SPI2_CONF_REG                         | SPI2 configuration register                                                 | 0x0094    | varies |
| PCR_SPI2_CLKMK_CONF_REG                   | SPI2_CLKMK configuration register                                          | 0x0098    | R/W    |
| PCR_SHA_CONF_REG                          | SHA configuration register                                                  | 0x00A0    | varies |
| PCR_ECC_CONF_REG                           | ECC configuration register                                                  | 0x00AC    | varies |
| PCR_ECC_PD_CTRL_REG                        | ECC power control register                                                  | 0x00B0    | R/W    |
| PCR_ECDSA_CONF_REG                         | ECDSA configuration register                                                 | 0x00BC    | varies |
| PCR_IOMUX_CONF_REG                         | IOMUX configuration register                                                 | 0x00C0    | R/W    |
| PCR_IOMUX_CLK_CONF_REG                     | IOMUX_CLK configuration register                                             | 0x00C4    | R/W    |
| PCR_TCM_MEM_MONITOR_CONF_REG              | TCM_MEM_MONITOR configuration register                                      | 0x00C8    | varies |
| PCR_PSRAM_MEM_MONITOR_CONF_REG            | PSRAM_MEM_MONITOR configuration register                                    | 0x00CC    | varies |
| PCR_TRACE_CONF_REG                         | TRACE configuration register                                                  | 0x00D0    | R/W    |
| PCR_ASSIST_CONF_REG                        | ASSIST configuration register                                                 | 0x00D4    | R/W    |
| PCR_CACHE_CONF_REG                         | CACHE configuration register                                                  | 0x00D8    | R/W    |
| PCR_CACHE_PD_CTRL_REG                      | CACHE power control register                                                  | 0x00DC    | R/W    |
| PCR_TIMEOUT_CONF_REG                       | TIMEOUT configuration register                                                 | 0x00E4    | R/W    |
| PCR_SYSCLK_CONF_REG                        | SYSCLK configuration register                                                  | 0x00E8    | varies |
| PCR_CPU_WAITI_CONF_REG                      | CPU_WAITI configuration register                                              | 0x00EC    | R/W    |
| PCR_CPU_FREQ_CONF_REG                       | CPU_FREQ configuration register                                                | 0x00F0    | R/W    |
| PCR_AHB_FREQ_CONF_REG                       | AHB_FREQ configuration register                                                 | 0x00F4    | R/W    |
| PCR_APB_FREQ_CONF_REG                       | APB_FREQ configuration register                                                 | 0x00F8    | R/W    |
| PCR_PLL_DIV_CLK_EN_REG                      | PLL DIV clock-gating configuration register                                   | 0x0100    | R/W    |
| PCR_CTRL_32K_CONF_REG                       | 32 kHz clock configuration register                                            | 0x010C    | R/W    |
| PCR_SEC_CONF_REG                            | Clock source configuration register for External Memory Encryption and Decryption | 0x0118    | R/W    |
| PCR_BUS_CLK_UPDATE_REG                      | Configuration register for applying updated high-performance system clock sources | 0x0120    | R/W/W/WT/C |
| PCR_SAR_CLK_DIV_REG                          | SAR ADC clock divisor configuration register                                   | 0x0124    | R/W    |
| PCR_TIMERGROUP_WDT_CONF_REG                 | TIMERGROUP_WDT configuration register                                         | 0x012C    | R/W    |
| PCR_TIMERGROUP_XTAL_CONF_REG                | TIMERGROUP1 configuration register                                            | 0x0130    | R/W    |
| PCR_ETM_CONF_REG                             | ETM configuration register                                                     | 0x013C    | varies |
| **Version Register**                         |                                                                                   |           |        |
| PCR_DATE_REG                                 | Version control register.                                                       | 0x0FFC     | R/W    |
```