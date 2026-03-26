

```markdown
| Name                                 | Description                                                                                   | Address   | Access PI | PL | PG |
|--------------------------------------|-----------------------------------------------------------------------------------------------|-----------|---------|----|----|
| Data Memory                          | See Table 31.6-1.                                                                             |           |         |    |    |
| Configuration Registers              |                                           |           |         |    |    |
| ECDSA_CONF_REG                       | ECDSA_DS configuration register                                                             | 0x0004    | R/W     | N/A|    |
| ECDSA_START_REG                      | ECDSA_DS start register                                                                      | 0x001C    | WT      |    |    |
| Clock and Reset Register             |                                           |           |         |    |    |
| ECDSA_CLK_REG                        | ECDSA_DS clock gate register                                                                | 0x0008    | R/W     | N/A|    |
| Interrupt Registers                  |                                           |           |         |    |    |
| ECDSA_INT_RAW_REG                    | ECDSA_DS interrupt raw register                                                             | 0x000C    | RO/WTC/SS|      |    |
| ECDSA_INT_ST_REG                     | ECDSA_DS interrupt status register                                                          | 0x0010    | RO      |    |    |
| ECDSA_INT_ENA_REG                    | ECDSA_DS interrupt enable register                                                         | 0x0014    | R/W     |    |    |
| ECDSA_INT_CLR_REG                    | ECDSA_DS interrupt clear register                                                          | 0x0018    | WT      |    |    |
| Status Registers                     |                                           |           |         |    |    |
| ECDSA_STATE_REG                      | ECDSA_DS state register                                                                      | 0x0020    | RO      |    |    |
| Result Register                      |                                           |           |         |    |    |
| ECDSA_RESULT_REG                     | ECDSA_DS result register                                                                     | 0x0024    | RO/SS   | N/A|    |
| SHA Registers                        |                                           |           |         |    |    |
| ECDSA_SHA_MODE_REG                   | ECDSA_DS controlling SHA register (Hash algorithm)                                          | 0x0200    | N/A     | R/W| N/A|
| ECDSA_SHA_START_REG                  | ECDSA_DS controlling SHA register (operation)                                               | 0x0210    | N/A     | WT | N/A|
| ECDSA_SHA_CONTINUE_REG               | ECDSA_DS controlling SHA register (operation)                                               | 0x0214    | N/A     | WT | N/A|
| ECDSA_SHA_BUSY_REG                   | ECDSA_DS controlling SHA status register                                                    | 0x0218    | N/A     | RO | N/A|
| Version Register                     |                                           |           |         |    |    |
| ECDSA_DATE_REG                       | Version control register                                                                     | 0x00FC    | R/W     | N/A|    |
```