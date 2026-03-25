

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LP_APM_REGION5_ATTR_REG                   | Region access permissions configuration register                          | 0x0048    | R/W    |
| LP_APM_REGION6_ATTR_REG                   | Region access permissions configuration register                          | 0x0054    | R/W    |
| LP_APM_REGION7_ATTR_REG                   | Region access permissions configuration register                          | 0x0060    | R/W    |
| LP_APM_FUNC_CTRL_REG                      | APM access path permission management register                             | 0x00C4    | R/W    |

**Status Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LP_APM_MO_STATUS_REG                      | LP_APM_CTRL MO status register                                             | 0x00C8    | RO     |
| LP_APM_MO_STATUS_CLR_REG                  | LP_APM_CTRL MO status clear register                                       | 0x00CC    | WT     |
| LP_APM_MO_EXCEPTION_INFO0_REG             | LP_APM_CTRL MO exception information register                              | 0x00D0    | RO     |
| LP_APM_MO_EXCEPTION_INFO1_REG             | LP_APM_CTRL MO exception information register                              | 0x00D4    | RO     |

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LP_APM_M1_STATUS_REG                      | LP_APM_CTRL M1 status register                                             | 0x00D8    | RO     |
| LP_APM_M1_STATUS_CLR_REG                  | LP_APM_CTRL M1 status clear register                                       | 0x00DC    | WT     |
| LP_APM_M1_EXCEPTION_INFO0_REG             | LP_APM_CTRL M1 exception information register                              | 0x00E0    | RO     |
| LP_APM_M1_EXCEPTION_INFO1_REG             | LP_APM_CTRL M1 exception information register                              | 0x00E4    | RO     |

**Interrupt Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LP_APM_INT_EN_REG                         | LP_APM_CTRL MO/1 interrupt enable register                                | 0x00E8    | R/W    |

**Clock Gating Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LP_APM_CLOCK_GATE_REG                     | Clock gating register                                                      | 0x00EC    | R/W    |

**Version Control Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LP_APM_DATE_REG                           | Version control register                                                   | 0x00FC    | R/W    |
```

## 18.8.3 LP_APMO_REG

The addresses in this section are relative to the LP_APMO base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                             |           |        |
| LP_APMO_REGION_FILTER_EN_REG              | Region enable register                                                     | 0x0000    | R/W    |
| LP_APMO_REGION0_ADDR_START_REG            | Region address register                                                    | 0x0004    | R/W    |
| LP_APMO_REGION0_ADDR_END_REG              | Region address register                                                    | 0x0008    | R/W    |
| LP_APMO_REGION1_ADDR_START_REG            | Region address register                                                    | 0x0010    | R/W    |
| LP_APMO_REGION1_ADDR_END_REG              | Region address register                                                    | 0x0014    | R/W    |
| LP_APMO_REGION2_ADDR_START_REG            | Region address register                                                    | 0x001C    | R/W    |
```