

```markdown
| Name                         | Description                                                                 | Address   | Access |
|------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| UART_POSPULSE_REG            | Autobaud high pulse register                                                | 0x0074    | RO     |
| UART_NEGPULSE_REG            | Autobaud low pulse register                                                 | 0x0078    | RO     |
| UART_LOWPULSE_REG            | Autobaud minimum low pulse duration register                                | 0x007C    | RO     |
| UART_HIGHPULSE_REG           | Autobaud minimum high pulse duration register                               | 0x0080    | RO     |
| UART_RXD_CNT_REG             | Autobaud edge change count register                                         | 0x0084    | RO     |
| **Version Register**         |                                                                             |           |        |
| UART_DATE_REG                | UART version control register                                               | 0x008C    | R/W    |

### 28.6.2 UHCI Register Summary

The addresses in this section are relative to UHCI base address provided in Table 4.3-2 in Chapter 4 System and Memory.

| Name                         | Description                                                                 | Address   | Access |
|------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration Register**   |                                                                             |           |        |
| UHCI_CONF0_REG               | UHCI configuration register                                                | 0x0000    | R/W    |
| UHCI_CONF1_REG               | UHCI configuration register                                                | 0x0014    | varies |
| UHCI_ESCAPE_CONF_REG         | Escape character configuration                                             | 0x0020    | R/W    |
| UHCI_HUNG_CONF_REG           | Timeout configuration                                                      | 0x0024    | R/W    |
| UHCI_ACK_NUM_REG             | UHCI ACK number configuration                                              | 0x0028    | varies |
| UHCI_QUICK_SENT_REG          | UHCI quick send configuration register                                     | 0x0030    | varies |
| UHCI_REG_Q0_WORD0_REG        | Q0 WORD0 quick send register                                               | 0x0034    | R/W    |
| UHCI_REG_Q0_WORD1_REG        | Q0 WORD1 quick send register                                               | 0x0038    | R/W    |
| UHCI_REG_Q1_WORD0_REG        | Q1 WORD0 quick send register                                               | 0x003C    | R/W    |
| UHCI_REG_Q1_WORD1_REG        | Q1 WORD1 quick send register                                               | 0x0040    | R/W    |
| UHCI_REG_Q2_WORD0_REG        | Q2 WORD0 quick send register                                               | 0x0044    | R/W    |
| UHCI_REG_Q2_WORD1_REG        | Q2 WORD1 quick send register                                               | 0x0048    | R/W    |
| UHCI_REG_Q3_WORD0_REG        | Q3 WORD0 quick send register                                               | 0x004C    | R/W    |
| UHCI_REG_Q3_WORD1_REG        | Q3 WORD1 quick send register                                               | 0x0050    | R/W    |
| UHCI_REG_Q4_WORD0_REG        | Q4 WORD0 quick send register                                               | 0x0054    | R/W    |
| UHCI_REG_Q4_WORD1_REG        | Q4 WORD1 quick send register                                               | 0x0058    | R/W    |
| UHCI_REG_Q5_WORD0_REG        | Q5 WORD0 quick send register                                               | 0x005C    | R/W    |
| UHCI_REG_Q5_WORD1_REG        | Q5 WORD1 quick send register                                               | 0x0060    | R/W    |
| UHCI_REG_Q6_WORD0_REG        | Q6 WORD0 quick send register                                               | 0x0064    | R/W    |
| UHCI_REG_Q6_WORD1_REG        | Q6 WORD1 quick send register                                               | 0x0068    | R/W    |
| UHCI_ESC_CONF0_REG            | Escape sequence configuration register 0                                   | 0x006C    | R/W    |
| UHCI_ESC_CONF1_REG            | Escape sequence configuration register 1                                   | 0x0070    | R/W    |
| UHCI_ESC_CONF2_REG            | Escape sequence configuration register 2                                   | 0x0074    | R/W    |
| UHCI_ESC_CONF3_REG            | Escape sequence configuration register 3                                   | 0x0078    | R/W    |
| UHCI_PKT_THRES_REG           | Configuration register for packet length                                   | 0x007C    | R/W    |
| **UHCI Interrupt Register**   |                                                                             |           |        |
| UHCI_INT_RAW_REG             | Raw interrupt status                                                        | 0x0004     | varies |
| UHCI_INT_ST_REG              | Masked interrupt status                                                     | 0x0008     | RO     |
```