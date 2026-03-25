

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CPU_APM_REGION6_ATTR_REG                  | Region access permissions configuration register                           | 0x0054  | R/W    |
| CPU_APM_REGION7_ATTR_REG                  | Region access permissions configuration register                           | 0x0060  | R/W    |
| CPU_APM_FUNC_CTRL_REG                     | APM access path permission management register                             | 0x00C4  | R/W    |

**Status Registers**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CPU_APM_MO_STATUS_REG                     | CPU_APM_CTRL MO status register                                            | 0x00C8  | RO     |
| CPU_APM_MO_STATUS_CLR_REG                 | CPU_APM_CTRL MO status clear register                                      | 0x00CC  | WT     |
| CPU_APM_MO_EXCEPTION_INFO0_REG            | CPU_APM_CTRL MO exception information register                             | 0x00D0  | RO     |
| CPU_APM_MO_EXCEPTION_INFO1_REG            | CPU_APM_CTRL MO exception information register                             | 0x00D4  | RO     |

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CPU_APM_M1_STATUS_REG                     | CPU_APM_CTRL M1 status register                                            | 0x00D8  | RO     |
| CPU_APM_M1_STATUS_CLR_REG                 | CPU_APM_CTRL M1 status clear register                                      | 0x00DC  | WT     |
| CPU_APM_M1_EXCEPTION_INFO0_REG            | CPU_APM_CTRL M1 exception information register                             | 0x00E0  | RO     |
| CPU_APM_M1_EXCEPTION_INFO1_REG            | CPU_APM_CTRL M1 exception information register                             | 0x00E4  | RO     |

**Interrupt Registers**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CPU_APM_INT_EN_REG                        | CPU_APM_CTRL MO/1 interrupt enable register                               | 0x0118  | R/W    |

**Clock Gating Registers**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CPU_APM_CLOCK_GATE_REG                    | Clock gating register                                                      | 0x07F8  | R/W    |

**Version Control Registers**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CPU_APM_DATE_REG                          | Version control register                                                   | 0x07FC  | R/W    |
```

## 16.8.4 HP_TEE_REG

The addresses in this section are relative to the Trusted Execution Environment (TEE) Register provided in Table 4-3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| **Configuration Registers**                |                                                                             |         |        |
| TEE_MO_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x0000  | R/W    |
| TEE_M1_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x0004  | R/W    |
| TEE_M2_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x0008  | R/W    |
| TEE_M3_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x000C  | R/W    |
| TEE_M4_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x0010  | R/W    |
| TEE_M5_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x0014  | R/W    |
| TEE_M6_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x0018  | R/W    |
| TEE_M7_MODE_CTRL_REG                      | Security mode configuration register                                      | 0x001C  | R/W    |
```