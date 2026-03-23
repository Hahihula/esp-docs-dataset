
```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                              |           |        |
| USB_SERIAL_JTAG_EP1_REG                    | FIFO access for the CDC-ACM data IN and OUT endpoints                                           | 0x0000    | R/W    |
| USB_SERIAL_JTAG_CONFO_REG                  | PHY hardware configuration                                                                      | 0x0018    | R/W    |
| USB_SERIAL_JTAG_TEST_REG                   | Registers used for debugging the PHY                                                            | 0x001C    | R/W    |
| USB_SERIAL_JTAG_MISC_CONF_REG              | Clock enable control                                                                            | 0x0044    | R/W    |
| USB_SERIAL_JTAG_MEM_CONF_REG               | Memory power control                                                                             | 0x0048    | R/W    |
| **Status Registers**                       |                                                                              |           |        |
| USB_SERIAL_JTAG_EP1_CONF_REG               | Configuration and control registers for the CDC-ACM FIFOs                                       | 0x0004    | varies |
| USB_SERIAL_JTAG_JFIFO_ST_REG               | JTAG FIFO status and control registers                                                          | 0x0020    | varies |
| USB_SERIAL_JTAG_FRAM_NUM_REG               | Last received SOF frame index register                                                         | 0x0024    | RO     |
| USB_SERIAL_JTAG_IN_EPO_STATUS              | Control IN endpoint status information                                                         | 0x0028    | RO     |
| USB_SERIAL_JTAG_IN_EP1_ST_REG              | CDC-ACM IN endpoint status information                                                        | 0x002C    | RO     |
| USB_SERIAL_JTAG_IN_EP2_ST_REG              | CDC-ACM interrupt IN endpoint status information                                               | 0x0030    | RO     |
| USB_SERIAL_JTAG_IN_EP3_ST_REG              | JTAG IN endpoint status information                                                            | 0x0034    | RO     |
| USB_SERIAL_JTAG_OUT_EPO_ST_REG             | Control OUT endpoint status information                                                        | 0x0038    | RO     |
| USB_SERIAL_JTAG_OUT_EP1_ST_REG             | CDC-ACM OUT endpoint status information                                                       | 0x003C    | RO     |
| USB_SERIAL_JTAG_OUT_EP2_ST_REG             | JTAG OUT endpoint status information                                                          | 0x0040    | RO     |
| **Interrupt Registers**                    |                                                                              |           |        |
| USB_SERIAL_JTAG_INT_RAW_REG                | Interrupt raw status register                                                                   | 0x0008    | R/WTC/SS|
| USB_SERIAL_JTAG_INT_ST_REG                 | Interrupt status register                                                                       | 0x000C    | RO     |
| USB_SERIAL_JTAG_INT_ENA_REG                | Interrupt enable status register                                                               | 0x0010    | R/W    |
| USB_SERIAL_JTAG_INT_CLR_REG                | Interrupt clear status register                                                                 | 0x0014    | WT     |
| **Version Registers**                      |                                                                              |           |        |
| USB_SERIAL_JTAG_DATE_REG                   | Version register                                                                                | 0x0080    | R/W    |
```