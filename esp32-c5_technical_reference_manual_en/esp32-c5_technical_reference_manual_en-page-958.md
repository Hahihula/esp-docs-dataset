

```markdown
| Name | Description | Address | Access PI | PL | PG | PB |
|:-------------------------------|:----------------------------------------------------------|:---------|:----------|:----|:----|:-----|
| Data Memory | See Table 28.7-1. | | | | | |
| Configuration Registers | | | | | | |
| ECDSA_CONF_REG | ECDSA configuration register | 0x0004 | R/W | | N/A | |
| ECDSA_START_REG | ECDSA start register | 0x001C | WT | | N/A | |
| Clock and Reset Register | | | | | | |
| ECDSA_CLK_REG | ECDSA clock gate register | 0x0008 | R/W | | N/A | |
| Interrupt Registers | | | | | | |
| ECDSA_INT_RAW_REG | ECDSA interrupt raw register | 0x000C | RO/WTCC/SS | | | |
| ECDSA_INT_ST_REG | ECDSA interrupt status register | 0x0010 | RO | | | |
| ECDSA_INT_ENA_REG | ECDSA interrupt enable register | 0x0014 | R/W | | | |
| ECDSA_INT_CLR_REG | ECDSA interrupt clear register | 0x0018 | WT | | | |
| Status Registers | | | | | | |
| ECDSA_STATE_REG | ECDSA state register | 0x0020 | RO | | | |
| Result Register | | | | | | |
| ECDSA_RESULT_REG | ECDSA result register | 0x0024 | RO/SS | | N/A | |
| SHA Registers | | | | | | |
| ECDSA_SHA_MODE_REG | ECDSA SHA-control register (Hash algorithm) | 0x0200 | N/A | R/W | N/A | |
| ECDSA_SHA_START_REG | ECDSA SHA-control register (operation) | 0x0210 | N/A | WT | N/A | |
| ECDSA_SHA_CONTINUE_REG | ECDSA SHA-control register (operation) | 0x0214 | N/A | WT | N/A | |
| ECDSA_SHA_BUSY_REG | ECDSA SHA-control status register | 0x0218 | N/A | RO | N/A | |
| Version Register | | | | | | |
| ECDSA_DATE_REG | Version control register | 0x00FC | R/W | | N/A | |
```