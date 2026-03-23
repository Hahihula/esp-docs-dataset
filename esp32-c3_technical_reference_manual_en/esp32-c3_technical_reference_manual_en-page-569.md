

```markdown
| Name                                 | Description                     | Address   | Access |
|--------------------------------------|---------------------------------|-----------|--------|
| UART_AT_CMD_GAPTOUT_REG             | Timeout configuration           | 0x0058    | R/W    |
| UART_AT_CMD_CHAR_REG                | AT escape sequence detection configuration | 0x005C  | R/W    |

**Version Register**

| Name                 | Description                     | Address   | Access |
|----------------------|---------------------------------|-----------|--------|
| UART_DATE_REG        | UART version control register   | 0x007C    | R/W    |
| UART_ID_REG          | UART ID register                | 0x0080    | varies |

**Configuration Register**

| Name                                 | Description                     | Address   | Access |
|--------------------------------------|---------------------------------|-----------|--------|
| UHCI_CONF0_REG                      | UHCI configuration register     | 0x0000    | R/W    |
| UHCI_CONF1_REG                      | UHCI configuration register     | 0x0014    | varies |
| UHCI_ESCAPE_CONF_REG                | Escape character configuration   | 0x0020    | R/W    |
| UHCI_HUNG_CONF_REG                  | Timeout configuration           | 0x0024    | R/W    |
| UHCI_ACK_NUM_REG                    | UHCI ACK number configuration    | 0x0028    | varies |
| UHCI_QUICK_SENT_REG                 | UHCI quick_sent configuration register | 0x0030 | varies |
| UHCI_REG_Q0_WORD0_REG               | Q0_WORD0 quick_sent register     | 0x0034    | R/W    |
| UHCI_REG_Q0_WORD1_REG               | Q0_WORD1 quick_sent register     | 0x0038    | R/W    |
| UHCI_REG_Q1_WORD0_REG               | Q1_WORD0 quick_sent register     | 0x003C    | R/W    |
| UHCI_REG_Q1_WORD1_REG               | Q1_WORD1 quick_sent register     | 0x0040    | R/W    |
| UHCI_REG_Q2_WORD0_REG               | Q2_WORD0 quick_sent register     | 0x0044    | R/W    |
| UHCI_REG_Q2_WORD1_REG               | Q2_WORD1 quick_sent register     | 0x0048    | R/W    |
| UHCI_REG_Q3_WORD0_REG               | Q3_WORD0 quick_sent register     | 0x004C    | R/W    |
| UHCI_REG_Q3_WORD1_REG               | Q3_WORD1 quick_sent register     | 0x0050    | R/W    |
| UHCI_REG_Q4_WORD0_REG               | Q4_WORD0 quick_sent register     | 0x0054    | R/W    |
| UHCI_REG_Q4_WORD1_REG               | Q4_WORD1 quick_sent register     | 0x0058    | R/W    |
| UHCI_REG_Q5_WORD0_REG               | Q5_WORD0 quick_sent register     | 0x005C    | R/W    |
| UHCI_REG_Q5_WORD1_REG               | Q5_WORD1 quick_sent register     | 0x0060    | R/W    |
| UHCI_REG_Q6_WORD0_REG               | Q6_WORD0 quick_sent register     | 0x0064    | R/W    |
| UHCI_REG_Q6_WORD1_REG               | Q6_WORD1 quick_sent register     | 0x0068    | R/W    |
| UHCI_ESC_CONF0_REG                  | Escape sequence configuration register 0 | 0x006C | R/W    |
| UHCI_ESC_CONF1_REG                  | Escape sequence configuration register 1 | 0x0070 | R/W    |
| UHCI_ESC_CONF2_REG                  | Escape sequence configuration register 2 | 0x0074 | R/W    |
| UHCI_ESC_CONF3_REG                  | Escape sequence configuration register 3 | 0x0078 | R/W    |
| UHCI_PKT_THRES_REG                  | Configuration register for packet length | 0x007C | R/W    |

**UHCI Interrupt Register**

| Name                 | Description                     | Address   | Access |
|----------------------|---------------------------------|-----------|--------|
| UHCI_INT_RAW_REG     | Raw interrupt status            | 0x0004    | varies |
| UHCI_INT_ST_REG      | Masked interrupt status         | 0x0008    | RO     |
| UHCI_INT_ENA_REG     | Interrupt enable bits           | 0x000C    | R/W    |
| UHCI_INT_CLR_REG     | Interrupt clear bits            | 0x0010    | WT     |

**UHCI Status Register**

| Name                 | Description                     | Address   | Access |
|----------------------|---------------------------------|-----------|--------|
| UHCI_STATE0_REG      | UHCI receive status             | 0x0018    | RO     |
| UHCI_STATE1_REG      | UHCI transmit status            | 0x001C    | RO     |
| UHCI_RX_HEAD_REG     | UHCI packet header register     | 0x002C    | RO     |

**Version Register**
```