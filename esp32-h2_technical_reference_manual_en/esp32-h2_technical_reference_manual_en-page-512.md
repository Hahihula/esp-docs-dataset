

```markdown
| Name                        | Description                  | Address   | Access |
|-----------------------------|------------------------------|-----------|--------|
| HP_APM_DATE_REG             | Version control register     | 0x07FC    | R/W    |

## 15.7.2 APM Registers of LP System (LP_APM_REG)

The addresses in this section are relative to the Low-Power Access Permission Management (LP_APM) base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                                        | Description                                       | Address         | Access |
|-------------------------------------------------------------|---------------------------------------------------|-----------------|--------|
| **Configuration Registers**                                 |                                                   |                 |        |
| LP_APM_REGION_FILTER_EN_REG                                | Region enable register                           | 0x0000          | R/W    |
| LP_APM_REGIONn_ADDR_START_REG (n: 0-3)                     | Region address register                          | 0x0004+0xC*n    | R/W    |
| LP_APM_REGIONn_ADDR_END_REG (n: 0-3)                       | Region address register                          | 0x0008+0xC*n    | R/W    |
| LP_APM_REGIONn_ATTR_REG (n: 0-3)                           | Region access permissions configuration register | 0x000C+0xC*n    | R/W    |
| LP_APM_FUNC_CTRL_REG                                       | APM access path permission management register   | 0x00C4          | R/W    |
| **Status Registers**                                       |                                                   |                 |        |
| LP_APM_MO_STATUS_REG                                       | LP_APM_CTRL MO status register                   | 0x00C8          | RO     |
| LP_APM_MO_STATUS_CLR_REG                                   | LP_APM_CTRL MO status clear register             | 0x00CC          | WT     |
| LP_APM_MO_EXCEPTION_INFO0_REG                              | LP_APM_CTRL MO exception information register    | 0x00D0          | RO     |
| LP_APM_MO_EXCEPTION_INFO1_REG                              | LP_APM_CTRL MO exception information register    | 0x00D4          | RO     |
| **Interrupt Registers**                                    |                                                   |                 |        |
| LP_APM_INT_EN_REG                                          | LP_APM_CTRL MO interrupt enable register         | 0x00E8          | R/W    |
| **Clock Gating Registers**                                 |                                                   |                 |        |
| LP_APM_CLOCK_GATE_REG                                      | Clock gating register                            | 0x00EC          | R/W    |
| **Version Control Registers**                              |                                                   |                 |        |
| LP_APM_DATE_REG                                            | Version control register                         | 0x00FC          | R/W    |

## 15.7.3 TEE Registers of HP System

The addresses in this section are relative to the Trusted Execution Environment (TEE) Register provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                        | Description                          | Address         | Access |
|-----------------------------|--------------------------------------|-----------------|--------|
| **Configuration Registers** |                                      |                 |        |
| TEE_Mn_MODE_CTRL_REG (n: 0-31)| Security mode configuration register | 0x0000+0x4*n    | R/W    |
```