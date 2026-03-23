

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| MO exception_info1 register                | HP_APM_MO_EXCEPTION_INFO1_REG                                                | 0x00D4    | RO     |
| M1 status register                         | HP_APM_M1_STATUS_REG                                                        | 0x00D8    | RO     |
| M1 status clear register                   | HP_APM_M1_STATUS_CLR_REG                                                    | 0x00DC    | WT     |
| M1 exception_info0 register                | HP_APM_M1_EXCEPTION_INFO0_REG                                               | 0x00E0    | RO     |
| M1 exception_info1 register                | HP_APM_M1_EXCEPTION_INFO1_REG                                               | 0x00E4    | RO     |
| M2 status register                         | HP_APM_M2_STATUS_REG                                                        | 0x00E8    | RO     |
| M2 status clear register                   | HP_APM_M2_STATUS_CLR_REG                                                    | 0x00EC    | WT     |
| M2 exception_info0 register                | HP_APM_M2_EXCEPTION_INFO0_REG                                               | 0x00F0    | RO     |
| M2 exception_info1 register                | HP_APM_M2_EXCEPTION_INFO1_REG                                               | 0x00F4    | RO     |
| M3 status register                         | HP_APM_M3_STATUS_REG                                                        | 0x00F8    | RO     |
| M3 status clear register                   | HP_APM_M3_STATUS_CLR_REG                                                    | 0x00FC    | WT     |
| M3 exception_info0 register                | HP_APM_M3_EXCEPTION_INFO0_REG                                               | 0x0100    | RO     |
| M3 exception_info1 register                | HP_APM_M3_EXCEPTION_INFO1_REG                                               | 0x0104    | RO     |
| APM interrupt enable register              | HP_APM_INT_EN_REG                                                           | 0x0108    | R/W    |
| Clock gating register                      | HP_APM_CLOCK_GATE_REG                                                       | 0x010C    | R/W    |
| Version control register                   | HP_APM_DATE_REG                                                             | 0x07FC    | R/W    |

### 16.6.2 Low Power APM Registers (LP_APM_REG)

The addresses in this section are relative to the Low-Power Access Permission Management (LP_APM) base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Region filter enable register              | LP_APM_REGION_FILTER_EN_REG                                                 | 0x0000    | R/W    |
| Region address register                    |                                                                             |           |        |
```