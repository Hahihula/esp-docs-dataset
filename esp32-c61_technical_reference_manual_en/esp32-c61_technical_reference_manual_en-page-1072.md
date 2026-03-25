

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                              |           |        |
| USB_SERIAL_JTAG_EP1_REG                    | FIFO access for the CDC-ACM data IN and OUT endpoints                                          | 0x0000    | R/W    |
| USB_SERIAL_JTAG_EP1_CONF_REG               | Configuration and control registers for the CDC-ACM FIFOs                                       | 0x0004    | varies |
| USB_SERIAL_JTAG_CONFO_REG                  | PHY hardware configuration                                                                      | 0x0018    | R/W    |
| USB_SERIAL_JTAG_TEST_REG                   | Registers used for debugging the PHY                                                          | 0x001C    | varies |
| USB_SERIAL_JTAG_MISC_CONF_REG              | Clock enable control                                                                            | 0x0044    | R/W    |
| USB_SERIAL_JTAG_MEM_CONF_REG               | Memory power control                                                                            | 0x0048    | R/W    |
| USB_SERIAL_JTAG_CHIP_RST_REG               | CDC-ACM chip reset control                                                                      | 0x004C    | varies |
| USB_SERIAL_JTAG_GET_LINE_CODE_WO_REG       | WO of GET_LINE_CODING command                                                                  | 0x0058    | R/W    |
| USB_SERIAL_JTAG_GET_LINE_CODE_W1_REG       | W1 of GET_LINE_CODING command                                                                  | 0x005C    | R/W    |
| USB_SERIAL_JTAG_CONFIG_UPDATE_REG          | Configuration registers' value update                                                          | 0x0060    | WT     |
| USB_SERIAL_JTAG_SER_AFIFO_CONFIG_REG       | Serial AFIFO configure register                                                                | 0x0064    | varies |
| USB_SERIAL_JTAG_SERIAL_EP_TIMEOUT_REG      | USB UART out endpoint timeout configuration                                                   | 0x006C    | varies |
| USB_SERIAL_JTAG_SERIAL_EP_TIMEOUT1_REG     | USB UART out endpoint timeout configuration                                                   | 0x0070    | R/W    |
| **Interrupt Registers**                    |                                                                              |           |        |
| USB_SERIAL_JTAG_INT_RAW_REG                | Interrupt raw status register                                                                   | 0x0008    | R/WTC/SS|
| USB_SERIAL_JTAG_INT_ST_REG                 | Interrupt status register                                                                       | 0x000C    | RO     |
| USB_SERIAL_JTAG_INT_ENA_REG                | Interrupt enable status register                                                               | 0x0010    | R/W    |
| USB_SERIAL_JTAG_INT_CLR_REG                | Interrupt clear status register                                                                | 0x0014    | WT     |
| **Status Registers**                       |                                                                              |           |        |
| USB_SERIAL_JTAG_JFIFO_ST_REG               | JTAG FIFO status and control registers                                                         | 0x0020    | varies |
| USB_SERIAL_JTAG_FRAM_NUM_REG               | Last received SOF frame index register                                                        | 0x0024    | RO     |
| USB_SERIAL_JTAG_IN_EPO_ST_REG              | Control IN endpoint status information                                                        | 0x0028    | RO     |
| USB_SERIAL_JTAG_IN_EP1_ST_REG              | CDC-ACM IN endpoint status information                                                        | 0x002C    | RO     |
| USB_SERIAL_JTAG_IN_EP2_ST_REG              | CDC-ACM interrupt IN endpoint status information                                               | 0x0030    | RO     |
| USB_SERIAL_JTAG_IN_EP3_ST_REG              | JTAG IN endpoint status information                                                           | 0x0034    | RO     |
| USB_SERIAL_JTAG_OUT_EPO_ST_REG             | Control OUT endpoint status information                                                       | 0x0038    | RO     |
```