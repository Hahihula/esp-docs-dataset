

```markdown
| Name                        | Description                  | Address   | Access |
|-----------------------------|------------------------------|-----------|--------|
| Clock Gating Registers      |                              |           |        |
| HP_APM_CLOCK_GATE_REG       | Clock gating register        | 0x07F8    | R/W    |
| Version Control Registers   |                              |           |        |
| HP_APM_DATE_REG             | Version control register     | 0x07FC    | R/W    |

16.8.2 LP_APM_REG

The addresses in this section are relative to the Low-Power Access Permission Management (LP_APM) base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                               | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------|-----------|--------|
| Configuration Registers                    |                                                           |           |        |
| LP_APM_REGION_FILTER_EN_REG                | Region enable register                                    | 0x0000    | R/W    |
| LP_APM_REGIONO_ADDR_START_REG              | Region address register                                   | 0x0004    | R/W    |
| LP_APM_REGIONO_ADDR_END_REG                | Region address register                                   | 0x0008    | R/W    |
| LP_APM_REGION1_ADDR_START_REG              | Region address register                                   | 0x0010    | R/W    |
| LP_APM_REGION1_ADDR_END_REG                | Region address register                                   | 0x0014    | R/W    |
| LP_APM_REGION2_ADDR_START_REG              | Region address register                                   | 0x001C    | R/W    |
| LP_APM_REGION2_ADDR_END_REG                | Region address register                                   | 0x0020    | R/W    |
| LP_APM_REGION3_ADDR_START_REG              | Region address register                                   | 0x0028    | R/W    |
| LP_APM_REGION3_ADDR_END_REG                | Region address register                                   | 0x002C    | R/W    |
| LP_APM_REGIONO_ATTR_REG                    | Region access permissions configuration register          | 0x000C    | R/W    |
| LP_APM_REGION1_ATTR_REG                    | Region access permissions configuration register          | 0x0018    | R/W    |
| LP_APM_REGION2_ATTR_REG                    | Region access permissions configuration register          | 0x0024    | R/W    |
| LP_APM_REGION3_ATTR_REG                    | Region access permissions configuration register          | 0x0030    | R/W    |
| LP_APM_FUNC_CTRL_REG                       | APM access path permission management register            | 0x00C4     | R/W    |
| Status Registers                           |                                                           |           |        |
| LP_APM_MO_STATUS_REG                       | LP_APM_CTRL MO status register                            | 0x00C8     | RO     |
| LP_APM_MO_STATUS_CLR_REG                   | LP_APM_CTRL MO status clear register                      | 0x00CC     | WT     |
| LP_APM_MO_EXCEPTION_INFO0_REG              | LP_APM_CTRL MO exception information register             | 0x00D0     | RO     |
| LP_APM_MO_EXCEPTION_INFO1_REG              | LP_APM_CTRL MO exception information register             | 0x00D4     | RO     |
| Interrupt Registers                        |                                                           |           |        |
| LP_APM_INT_EN_REG                          | LP_APM_CTRL MO interrupt enable register                  | 0x00E8     | R/W    |
| Clock Gating Registers                     |                                                           |           |        |
```