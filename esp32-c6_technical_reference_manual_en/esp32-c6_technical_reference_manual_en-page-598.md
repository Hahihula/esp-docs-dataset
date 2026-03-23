
```markdown
| Name                                                                                       | Description                                                                                      | Address | Access |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| **Configuration Register**                                                                  |                                                                                  |         |        |
| HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG                                      | External device encryption/decryption configuration register                                    | 0x0000  | R/W    |
| HP_SYSTEM_SEC_DPA_CONF_REG                                                                 | HP anti-DPA security configuration register                                                     | 0x0008  | R/W    |
| HP_SYSTEM_CORE_DEBUG_RUNSTALL_CONF_REG                                                     | Core Debug RunStall configuration register                                                    | 0x0040  | R/W    |
| **CPU Peripheral Timeout Register**                                                        |                                                                                  |         |        |
| HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG                                                       | CPU Peripheral Timeout configuration register                                                 | 0x000C  | varies |
| HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG                                                       | Abnormal access address register                                                               | 0x0010  | RO     |
| HP_SYSTEM_CPU_PERI_TIMEOUT_UID_REG                                                        | Master ID and permission register                                                              | 0x0014  | WTC    |
| **HP Peripheral Timeout Register**                                                         |                                                                                  |         |        |
| HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG                                                        | HP Peripheral Timeout configuration register                                                 | 0x0018  | varies |
| HP_SYSTEM_HP_PERI_TIMEOUT_ADDR_REG                                                        | Abnormal access address register                                                               | 0x001C  | RO     |
| HP_SYSTEM_HP_PERI_TIMEOUT_UID_REG                                                         | Master ID and permission register                                                              | 0x0020  | WTC    |
| **LP Peripheral Timeout Register**                                                         |                                                                                  |         |        |
| LP_PERI_BUS_TIMEOUT_CONF_REG                                                               | LP Peripheral timeout configuration register                                                  | 0x0010  | varies |
| LP_PERI_BUS_TIMEOUT_ADDR_REG                                                              | LP Peripheral abnormal access address register                                                | 0x0014  | RO     |
| LP_PERI_BUS_TIMEOUT_UID_REG                                                               | LP Peripheral Master ID and permission register                                               | 0x0018  | WTC    |
| **Version Register**                                                                       |                                                                                  |         |        |
| HP_SYSTEM_DATE_REG                                                                         | Date control and version control register                                                     | 0x03FC  | R/W    |
```