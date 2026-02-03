**Title: Chapter 26 UART Controller (UART)**

**GoBack**

| Name                          | Description                                    | Address   | Access |
|-------------------------------|-----------------------------------------------|----------|--------|
| UHCI_INT_ST_REG              | Masked interrupt status                        | 0x0008   | RO     |
| UHCI_INT_ENA_REG             | Interrupt enable bits                         | 0x000C   | R/W    |
| UHCI_INT_CLR_REG             | Interrupt clear bits                           | 0x0010   | WT     |
| UHCI_APP_INT_SET_REG         | Software interrupt trigger source              | 0x0014   | WT     |
| **UHCI Status Register**      |                                               |          |        |
| UHCI_STATEO_REG              | UHCI receive status                             | 0x001C   | RO     |
| UHCI_STATE1_REG              | UHCI transmit status                            | 0x0020   | RO     |
| UHCI_RX_HEAD_REG             | UHCI packet header register                    | 0x0030   | RO     |
| **Version Register**          |                                               |          |        |
| UHCI_DATE_REG                | UHCI version control register                  | 0x0084   | R/W    |

---

*Espressif Systems*

946

ESP32-S3 TRM (Version 1.7)

[Submit Documentation Feedback](#)