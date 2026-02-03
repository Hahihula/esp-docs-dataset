**Table: Interrupt Registers**

| Name                                      | Description                                                                                   | Address   | Access |
|-------------------------------------------|------------------------------------------------------------------------------------------------|----------|--------|
| **Interrupt Registers**                  |                                                                                               |          |       |
| INTERRUPT\Core1_USB_DEVICE_INT_MAP_REG  | USB DEVICE interrupt configuration register                                                   | 0x0980   | R/W    |
| INTERRUPT\Core1_PERI_BACKUP_INT_MAP_REG  | PERI BACKUP interrupt configuration register                                                  | 0x0984   | R/W    |
| INTERRUPT\Core1_DMA_EXTMEM_REJECT_INT_MAP_REG | DMA_EXTMEM_REJECT interrupt configuration register | 0x0988   | R/W    |
| **Status Registers**                      |                                                                                               |          |        |
| INTERRUPT\Core1_INR_STATUS_0_REG         | Interrupt status register                                                                      | 0x098C   | RO     |
| INTERRUPT\Core1_INR_STATUS_1_REG         | Interrupt status register                                                                      | 0x0990   | RO     |
| INTERRUPT\Core1_INR_STATUS_2_REG         | Interrupt status register                                                                      | 0x0994   | RO     |
| INTERRUPT\Core1_INR_STATUS_3_REG         | Interrupt status register                                                                      | 0x0998   | RO     |
| **Clock Register**                        |                                                                                               |          |        |
| INTERRUPT\Core1_CLOCK_GATE_REG           | Clock gate register                                                                            | 0x099C   | R/W    |
| **Version Register**                      |                                                                                               |          |        |
| INTERRUPT\Core1_DATE_REG                 | Version control register                                                                        | 0x0FFC   | R/W    |

---

*Note: The table is structured with headers for different categories of interrupt registers, including Interrupt Registers and Status Registers. Each entry includes the name of a specific register or configuration parameter along with its description, address in hexadecimal format (0x prefix), access type (R/W - Read/Write; RO - Read Only).*

---

*Footer: ESP32-S3 TRM (Version 1.7)*