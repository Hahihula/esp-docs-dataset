

```markdown
| Name                                       | Description                  | Address   | Access |
|--------------------------------------------|------------------------------|-----------|--------|
| HP_SYSTEM_GPIO_O_HYS_CTRL1_REG             | HP GPIO hold control 1       | 0x01C4    | R/W    |

## 20.4.2 ICM Register Summary

The addresses in this section are relative to relative to AXI ICM base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                  | Address   | Access |
|--------------------------------------------|------------------------------|-----------|--------|
| Version Register                           | ICM version control          | 0x0000    | R/W    |
| Clock Gating Register                      | Clock gating control         | 0x0004    | R/W    |
| Status Register                            |                              |           |        |
| HP_SYSTEM_ICM_DLOCK_STATUS_REG             | ICM deadlock status          | 0x0008    | RO     |
| HP_SYSTEM_ICM_SYS_ADDRHOLE_ADDR_REG        | System address hole address   | 0x0038    | RO     |
| HP_SYSTEM_ICM_SYS_ADDRHOLE_INFO_REG        | System address hole information | 0x003C    | RO     |
| HP_SYSTEM_ICM_CPU_ADDRHOLE_ADDR_REG        | CPU address hole address      | 0x0040    | RO     |
| HP_SYSTEM_ICM_CPU_ADDRHOLE_INFO_REG        | CPU address hole information  | 0x0044    | RO     |
| Interrupt Register                         |                              |           |        |
| HP_SYSTEM_ICM_INT_RAW_REG                  | ICM interrupt raw status      | 0x000C    | R/WTC/SS|
| HP_SYSTEM_ICM_INT_ST_REG                   | ICM interrupt status          | 0x0010    | RO     |
| HP_SYSTEM_ICM_INT_ENA_REG                  | ICM interrupt enable          | 0x0014    | R/W    |
| HP_SYSTEM_ICM_INT_CLR_REG                  | ICM interrupt clear           | 0x0018    | WT     |
| Configuration Register                     |                              |           |        |
| HP_SYSTEM_ICM_SLV_ARB_PRIORITY_REG         | Slave arbitration priority configuration | 0x0024 | R/W   |
| HP_SYSTEM_ICM_MST_ARQOS_REGO_REG           | ARQoS configuration           | 0x0028    | R/W    |
| HP_SYSTEM_ICM_MST_AWQOS_REGO_REG           | AWQoS configuration           | 0x0030    | R/W    |
| HP_SYSTEM_ICM_DLOCK_TIMEOUT_REG            | ICM bus timeout configuration | 0x0048    | R/W    |

## 20.4.3 LP Register Summary

The addresses in this section are relative to LP System Registers base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                  | Address   | Access |
|--------------------------------------------|------------------------------|-----------|--------|
| Configuration & Control Registers          |                              |           |        |
| LP_SYSTEM_LP_SYS_VER_DATE_REG              | Version control              | 0x0000    | R/W    |
| LP_SYSTEM_SYS_CTRL_REG                     | System control               | 0x0008    | varies |
| LP_SYSTEM_LP_CLK_CTRL_REG                  | Clock control                | 0x000C    | R/W    |
| LP_SYSTEM_LP_RST_CTRL_REG                  | Reset control                | 0x0010    | R/W    |
```