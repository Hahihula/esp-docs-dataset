

```markdown
| Name                                       | Description                                                                 | Address     | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-------------|--------|
| PMS_CORE_X_IRAMO_PMS_CONSTRAIN_1_REG      | IBUS Permission Config Register 1                                          | 0x00AC      | R/WL   |
| PMS_CORE_X_IRAMO_PMS_CONSTRAIN_2_REG      | IBUS Permission Config Register 2                                          | 0x00B0      | R/WL   |
| PMS_CORE_O_IRAMO_PMS_MONITOR_O_REG        | CPUO IBUS Permission Interrupt Register 0                                  | 0x00B4      | R/WL   |
| PMS_CORE_O_IRAMO_PMS_MONITOR_1_REG         | CPUO IBUS Permission Interrupt Register 1                                  | 0x00B8      | R/WL   |
| PMS_CORE_X_DRAMO_PMS_CONSTRAIN_O_REG       | DBUS Permission Config Register 0                                          | 0x00C0      | R/WL   |
| PMS_CORE_X_DRAMO_PMS_CONSTRAIN_1_REG       | DBUS Permission Config Register 1                                          | 0x00C4      | R/WL   |
| PMS_CORE_O_DRAMO_PMS_MONITOR_O_REG         | CPUO dBUS Permission Interrupt Register 0                                 | 0x00C8      | R/WL   |
| PMS_CORE_O_DRAMO_PMS_MONITOR_1_REG          | CPUO dBUS Permission Interrupt Register 1                                 | 0x00CC      | R/WL   |
| PMS_CORE_O_PIF_PMS_CONSTRAIN_n_REG (n: 0 - 10) | Peripheral Permission Configuration Register n                           | 0x00D8 + 4 * n | R/WL   |
| PMS_REGION_PMS_CONSTRAIN_n_REG (n: 0 - 10) | CPU Split_Region Permission Register n                                    | 0x0104 + 4 * n | R/WL   |
| PMS_CORE_O_PIF_PMS_MONITOR_O_REG           | CPU PIF Permission Interrupt Register 0                                   | 0x0130      | R/WL   |
| PMS_CORE_O_PIF_PMS_MONITOR_1_REG            | CPU PIF Permission Interrupt Register 1                                   | 0x0134      | R/WL   |
| PMS_CORE_O_PIF_PMS_MONITOR_4_REG             | CPU PIF Permission Interrupt Register 4                                   | 0x0140      | R/WL   |

Status Register
| Name                                       | Description                                                                 | Address     | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-------------|--------|
| PMS_DMA_APBPERI_PMS_MONITOR_2_REG          | GDMA Permission Interrupt Register 2                                      | 0x0088      | RO     |
| PMS_DMA_APBPERI_PMS_MONITOR_3_REG           | GDMA Permission Interrupt Register 3                                      | 0x008C      | RO     |
| PMS_CORE_O_IRAMO_PMS_MONITOR_2_REG          | CPUO IBUS Permission Interrupt Register 2                                 | 0x00BC      | RO     |
| PMS_CORE_O_DRAMO_PMS_MONITOR_2_REG           | CPUO dBUS Permission Interrupt Register 2                                | 0x00D0      | RO     |
| PMS_CORE_O_DRAMO_PMS_MONITOR_3_REG           | CPUO dBUS Permission Interrupt Register 3                                | 0x00D4      | RO     |
| PMS_CORE_O_PIF_PMS_MONITOR_2_REG             | CPU PIF Permission Interrupt Register 2                                   | 0x0138      | RO     |
| PMS_CORE_O_PIF_PMS_MONITOR_3_REG              | CPU PIF Permission Interrupt Register 3                                   | 0x013C      | RO     |
| PMS_CORE_O_PIF_PMS_MONITOR_5_REG              | CPU PIF Permission Interrupt Register 5                                   | 0x0144      | RO     |
| PMS_CORE_O_PIF_PMS_MONITOR_6_REG              | CPU PIF Permission Interrupt Register 6                                   | 0x0148      | RO     |

Version Register
| Name                                       | Description                                                                 | Address     | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-------------|--------|
| PMS_CLOCK_GATE_REG_REG                     | Clock Gate Config Register                                                 | 0x0170      | R/W    |
| PMS_DATE_REG                               | Sensitive Version Register                                                | 0x0FFC      | R/W    |
```