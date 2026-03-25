

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| TEE_HP_SYSTEM_REG_CTRL_REG                | HP_SYSREG read/write control register                                                          | 0x0104  | R/W    |
| TEE_PCR_REG_CTRL_REG                      | PCR read/write control register                                                                | 0x0108  | R/W    |
| TEE_MSPI_CTRL_REG                         | SPI01 read/write control register                                                              | 0x010C  | R/W    |
| TEE_HP_APM_CTRL_REG                       | HP_APM and LP_APMO read/write control register                                                 | 0x0110  | varies |
| TEE_CPU_APM_CTRL_REG                      | CPU_APM_REG read/write control                                                                 | 0x0114  | varies |
| TEE_TEE_CTRL_REG                          | TEE read/write control register                                                                | 0x0118  | varies |
| TEE_CRYPTO_CTRL_REG                       | CRYPT read/write control register, including security peripherals from AES to ECDSA address range | 0x011C  | R/W    |
| TEE_TRACE_CTRL_REG                        | TRACE read/write control register                                                              | 0x0120  | R/W    |
| TEE_CPU_BUS_MONITOR_CTRL_REG              | BUS_MONITOR read/write control                                                                 | 0x0128  | R/W    |
| TEE_INTPRI_REG_CTRL_REG                   | INTPRI_REG read/write control register                                                        | 0x012C  | R/W    |
| TEE_TWAI1_CTRL_REG                        | TWAI1 read/write control register                                                              | 0x0138  | R/W    |
| TEE_SPI2_CTRL_REG                         | SPI2 read/write control register                                                               | 0x013C  | R/W    |
| TEE_BS_CTRL_REG                           | BITSCRAMBLER read/write control register                                                      | 0x0140  | R/W    |
| TEE_BUS_ERR_CONF_REG                      | Error message return configuration register                                                   | 0x0FF0  | R/W    |
| clock gating register                     |                                                                                                  |         |        |
| TEE_CLOCK_GATE_REG                        | Clock gating register                                                                           | 0x0FF8  | R/W    |
| Version Control Registers                 |                                                                                                  |         |        |
| TEE_DATE_REG                              | Version control register                                                                       | 0x0FFC  | R/W    |

### 18.8.6 LP_TEE_REG

The addresses in this section are relative to the LP_TEE base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| Configuration Registers                   |                                                                                                  |         |        |
| LP_TEE_MO_MODE_CTRL_REG                   | Security mode configuration register                                                           | 0x0000  | R/W    |
| Peripheral Read/Write Control Register    |                                                                                                  |         |        |
| LP_TEE_EFUSE_CTRL_REG                     | eFuse read/write control register                                                              | 0x0004  | R/W    |
| LP_TEE_PMU_CTRL_REG                       | PMU read/write control register                                                                | 0x0008  | R/W    |
| LP_TEE_CLKRST_CTRL_REG                    | LP_CLKRST read/write control register                                                          | 0x000C  | R/W    |
| LP_TEE_LP_AON_CTRL_CTRL_REG               | LP_AON read/write control register                                                             | 0x0010  | R/W    |
| LP_TEE_LP_TIMER_CTRL_REG                  | LP_TIMER read/write control register                                                          | 0x0014  | R/W    |
| LP_TEE_LP_WDT_CTRL_REG                    | LP_WDT read/write control register                                                            | 0x0018  | R/W    |
| LP_TEE_LP_PERI_CTRL_REG                   | LPPERI read/write control register                                                             | 0x001C  | R/W    |
```