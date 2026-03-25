

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| PCR_SEC_CONF_REG                          | Clock source configuration register for External Memory Encryption and Decryption               | 0x013C    | R/W    |
| PCR_BUS_CLK_UPDATE_REG                    | Configuration register for applying updated high-performance system clock sources              | 0x0144    | R/W/WTC|
| PCR_SAR_CLK_DIV_REG                       | SAR ADC clock divisor configuration register                                                  | 0x0148    | R/W    |
| PCR_BS_CONF_REG                           | BS configuration register                                                                       | 0x0150    | R/W    |
| PCR_BS_FUNC_CONF_REG                      | BS_FUNC_CLK configuration register                                                             | 0x0154    | R/W    |
| PCR_BS_PD_CTRL_REG                        | BS power control register                                                                       | 0x0158    | R/W    |
| PCR_TIMERGROUP_WDT_CONF_REG               | TIMERGROUP_WDT configuration register                                                          | 0x015C    | R/W    |
| PCR_TIMERGROUP_XTAL_CONF_REG              | TIMERGROUP1 configuration register                                                             | 0x0160    | R/W    |
| PCR_KM_CONF_REG                           | Key Manager configuration register                                                             | 0x0164    | R/W    |
| PCR_KM_PD_CTRL_REG                        | Key Manager power control register                                                             | 0x0168    | R/W    |
| PCR_TCM_MEM_MONITOR_CONF_REG              | TCM_MEM_MONITOR configuration register                                                         | 0x016C    | varies |
| PCR_PSRAM_MEM_MONITOR_CONF_REG            | PSRAM_MEM_MONITOR configuration register                                                      | 0x0170    | varies |
| PCR_HPCORE_O_PD_CTRL_REG                  | HP COREO power control register                                                                | 0x0178    | R/W    |
| PCR_SDIO_SLAVE_CONF_REG                   | SDIO_SLAVE configuration register                                                              | 0x017C    | R/W    |
| Frequency Statistics Register             |                                                                                                  |           |        |
| PCR_SYSCLK_FREQ_QUERY_O_REG               | SYSCLK frequency query O register                                                               | 0x0124    | HRO    |
| Version Register                          |                                                                                                  |           |        |
| PCR_DATE_REG                              | Date register                                                                                    | 0x0FFC    | R/W    |

## 9.4.2 LP System Clock Register Summary

The addresses of the last two registers with the LPPERI prefix in this section are relative to the Low-power Peripheral Register (LPPERI) base address. The other addresses in this section are relative to the Low-power Clock/Reset Register (LP_CLKRST) base address. For base address, please refer to Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| Configuration Registers                    |                                                                                                  |           |        |
| LP_CLKRST_LP_CLK_CONF_REG                 | LP system clock source configuration register                                                   | 0x0000    | R/W    |
| LP_CLKRST_LP_CLK_PO_EN_REG                | Configuration register for gating clock signals to pins                                        | 0x0004    | R/W    |
| LP_CLKRST_LP_CLK_EN_REG                   | Configuration register for gating LP clock source                                              | 0x0008    | R/W    |
```