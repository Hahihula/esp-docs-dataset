

```markdown
| Name                                       | Description                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------|-----------|--------|
| LP_APMO_REGION2_ADDR_END_REG               | Region address register                       | 0x0020    | R/W    |
| LP_APMO_REGION3_ADDR_START_REG             | Region address register                       | 0x0028    | R/W    |
| LP_APMO_REGION3_ADDR_END_REG               | Region address register                       | 0x002C    | R/W    |
| LP_APMO_REGION4_ADDR_START_REG             | Region address register                       | 0x0034    | R/W    |
| LP_APMO_REGION4_ADDR_END_REG               | Region address register                       | 0x0038    | R/W    |
| LP_APMO_REGION5_ADDR_START_REG             | Region address register                       | 0x0040    | R/W    |
| LP_APMO_REGION5_ADDR_END_REG               | Region address register                       | 0x0044    | R/W    |
| LP_APMO_REGION6_ADDR_START_REG             | Region address register                       | 0x004C    | R/W    |
| LP_APMO_REGION6_ADDR_END_REG               | Region address register                       | 0x0050    | R/W    |
| LP_APMO_REGION7_ADDR_START_REG             | Region address register                       | 0x0058    | R/W    |
| LP_APMO_REGION7_ADDR_END_REG               | Region address register                       | 0x005C    | R/W    |
| LP_APMO_REGION0_ATTR_REG                   | Region access permissions configuration register | 0x000C    | R/W    |
| LP_APMO_REGION1_ATTR_REG                   | Region access permissions configuration register | 0x0018    | R/W    |
| LP_APMO_REGION2_ATTR_REG                   | Region access permissions configuration register | 0x0024    | R/W    |
| LP_APMO_REGION3_ATTR_REG                   | Region access permissions configuration register | 0x0030    | R/W    |
| LP_APMO_REGION4_ATTR_REG                   | Region access permissions configuration register | 0x003C    | R/W    |
| LP_APMO_REGION5_ATTR_REG                   | Region access permissions configuration register | 0x0048    | R/W    |
| LP_APMO_REGION6_ATTR_REG                   | Region access permissions configuration register | 0x0054    | R/W    |
| LP_APMO_REGION7_ATTR_REG                   | Region access permissions configuration register | 0x0060    | R/W    |
| LP_APMO_FUNC_CTRL_REG                      | APM access path permission management register | 0x00C4     | R/W    |

**Status Registers**

| Name                                       | Description                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------|-----------|--------|
| LP_APMO_MO_STATUS_REG                      | LP_APMO_CTRL MO status register               | 0x00C8    | RO     |
| LP_APMO_MO_STATUS_CLR_REG                  | LP_APMO_CTRL MO status clear register         | 0x00CC    | WT     |
| LP_APMO_MO_EXCEPTION_INFO0_REG             | LP_APMO_CTRL MO exception information register | 0x00D0    | RO     |
| LP_APMO_MO_EXCEPTION_INFO1_REG             | LP_APMO_CTRL MO exception information register | 0x00D4    | RO     |

**Interrupt Registers**

| Name                                       | Description                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------|-----------|--------|
| LP_APMO_INT_EN_REG                         | LP_APMO_CTRL interrupt enable register        | 0x00D8    | R/W    |

**Clock Gating Registers**

| Name                                       | Description                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------|-----------|--------|
| LP_APMO_CLOCK_GATE_REG                     | Clock gating register                         | 0x00DC    | R/W    |

**Version Control Registers**

| Name                                       | Description                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------|-----------|--------|
| LP_APMO_DATE_REG                           | Version control register                      | 0x07FC    | R/W    |
```