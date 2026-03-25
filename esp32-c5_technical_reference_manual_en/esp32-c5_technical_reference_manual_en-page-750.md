

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| HP_APM_REGION11_ATTR_REG                  | Region access permissions configuration register                           | 0x0090    | R/W    |
| HP_APM_REGION12_ATTR_REG                  | Region access permissions configuration register                           | 0x009C    | R/W    |
| HP_APM_REGION13_ATTR_REG                  | Region access permissions configuration register                           | 0x00A8    | R/W    |
| HP_APM_REGION14_ATTR_REG                  | Region access permissions configuration register                           | 0x00B4    | R/W    |
| HP_APM_REGION15_ATTR_REG                  | Region access permissions configuration register                           | 0x00C0    | R/W    |
| HP_APM_FUNC_CTRL_REG                      | APM access path permission management register                              | 0x00C4    | R/W    |

**Status Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| HP_APM_M0_STATUS_REG                      | HP_APM_CTRL M0 status register                                             | 0x00C8    | RO     |
| HP_APM_M0_STATUS_CLR_REG                  | HP_APM_CTRL M0 status clear register                                       | 0x00CC    | WT     |
| HP_APM_M0_EXCEPTION_INFO0_REG             | HP_APM_CTRL M0 exception information register                              | 0x00D0    | RO     |
| HP_APM_M0_EXCEPTION_INFO1_REG             |                                                                             | 0x00D4    | RO     |
| HP_APM_M1_STATUS_REG                      | HP_APM_CTRL M1 status register                                             | 0x00D8    | RO     |
| HP_APM_M1_STATUS_CLR_REG                  | HP_APM_CTRL M1 status clear register                                       | 0x00DC    | WT     |
| HP_APM_M1_EXCEPTION_INFO0_REG             | HP_APM_CTRL M1 exception information register                              | 0x00E0    | RO     |
| HP_APM_M1_EXCEPTION_INFO1_REG             |                                                                             | 0x00E4    | RO     |
| HP_APM_M2_STATUS_REG                      | HP_APM_CTRL M2 status register                                             | 0x00E8    | RO     |
| HP_APM_M2_STATUS_CLR_REG                  | HP_APM_CTRL M2 status clear register                                       | 0x00EC    | WT     |
| HP_APM_M2_EXCEPTION_INFO0_REG             | HP_APM_CTRL M2 exception information register                              | 0x00F0    | RO     |
| HP_APM_M2_EXCEPTION_INFO1_REG             |                                                                             | 0x00F4    | RO     |
| HP_APM_M3_STATUS_REG                      | HP_APM_CTRL M3 status register                                             | 0x00F8    | RO     |
| HP_APM_M3_STATUS_CLR_REG                  | HP_APM_CTRL M3 status clear register                                       | 0x00FC    | WT     |
| HP_APM_M3_EXCEPTION_INFO0_REG             | HP_APM_CTRL M3 exception information register                              | 0x0100    | RO     |
| HP_APM_M3_EXCEPTION_INFO1_REG             |                                                                             | 0x0104    | RO     |
| HP_APM_M4_STATUS_REG                      | HP_APM_CTRL M4 status register                                             | 0x0108    | RO     |
| HP_APM_M4_STATUS_CLR_REG                  | HP_APM_CTRL M4 status clear register                                       | 0x010C    | WT     |
| HP_APM_M4_EXCEPTION_INFO0_REG             | HP_APM_CTRL M4 exception information register                              | 0x0110    | RO     |
| HP_APM_M4_EXCEPTION_INFO1_REG             |                                                                             | 0x0114    | RO     |

**Interrupt Registers**
```