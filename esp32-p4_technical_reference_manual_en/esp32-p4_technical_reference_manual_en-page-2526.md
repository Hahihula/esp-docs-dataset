
```markdown
## 48.7 Register Summary

The addresses in this section are relative to Pulse Count Controller base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Register** |  |  |  |
| PCNT_U0_CONF0_REG | Configuration register 0 for unit 0 | 0x0000 | R/W |
| PCNT_U0_CONF1_REG | Configuration register 1 for unit 0 | 0x0004 | R/W |
| PCNT_U0_CONF2_REG | Configuration register 2 for unit 0 | 0x0008 | R/W |
| PCNT_U1_CONF0_REG | Configuration register 0 for unit 1 | 0x000C | R/W |
| PCNT_U1_CONF1_REG | Configuration register 1 for unit 1 | 0x0010 | R/W |
| PCNT_U1_CONF2_REG | Configuration register 2 for unit 1 | 0x0014 | R/W |
| PCNT_U2_CONF0_REG | Configuration register 0 for unit 2 | 0x0018 | R/W |
| PCNT_U2_CONF1_REG | Configuration register 1 for unit 2 | 0x001C | R/W |
| PCNT_U2_CONF2_REG | Configuration register 2 for unit 2 | 0x0020 | R/W |
| PCNT_U3_CONF0_REG | Configuration register 0 for unit 3 | 0x0024 | R/W |
| PCNT_U3_CONF1_REG | Configuration register 1 for unit 3 | 0x0028 | R/W |
| PCNT_U3_CONF2_REG | Configuration register 2 for unit 3 | 0x002C | R/W |
| PCNT_CTRL_REG | Control register for all counters | 0x0060 | R/W |
| **Status Register** |  |  |  |
| PCNT_U0_CNT_REG | Counter value for unit 0 | 0x0030 | RO |
| PCNT_U1_CNT_REG | Counter value for unit 1 | 0x0034 | RO |
| PCNT_U2_CNT_REG | Counter value for unit 2 | 0x0038 | RO |
| PCNT_U3_CNT_REG | Counter value for unit 3 | 0x003C | RO |
| PCNT_U0_STATUS_REG | PNCT UNIT0 status register | 0x0050 | RO |
| PCNT_U1_STATUS_REG | PNCT UNIT1 status register | 0x0054 | RO |
| PCNT_U2_STATUS_REG | PNCT UNIT2 status register | 0x0058 | RO |
| PCNT_U3_STATUS_REG | PNCT UNIT3 status register | 0x005C | RO |
| **Interrupt Register** |  |  |  |
| PCNT_INT_RAW_REG | Interrupt raw status register | 0x0040 | RO |
| PCNT_INT_ST_REG | Interrupt status register | 0x0044 | RO |
| PCNT_INT_ENA_REG | Interrupt enable register | 0x0048 | R/W |
| PCNT_INT_CLR_REG | Interrupt clear register | 0x004C | WO |
| **Version Register** |  |  |  |
| PCNT_DATE_REG | PCNT version control register | 0x00FC | R/W |
```