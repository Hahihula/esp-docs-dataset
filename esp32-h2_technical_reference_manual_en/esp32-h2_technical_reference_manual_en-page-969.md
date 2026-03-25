

```markdown
Register 33.9. USB_SERIAL_JTAG_GET_LINE_CODE_W1_REG (0x005C)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-24     | (reserved)                                |                                                                             |
| 23        | USB_SERIAL_JTAG_GET_BDATA_BITS            | Configures the value of bDataBits set by software, which is requested by GET_LINE_CODING command. (R/W) |
| 22        | USB_SERIAL_JTAG_GET_BPARITY_TYPE          | Configures the value of bParityType set by software, which is requested by GET_LINE_CODING command. (R/W) |
| 15        | USB_SERIAL_JTAG_GET_BCHAR_FORMAT          | Configures the value of bCharFormat set by software, which is requested by GET_LINE_CODING command. (R/W) |

Register 33.10. USB_SERIAL_JTAG_CONFIG_UPDATE_REG (0x0060)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-1      | (reserved)                                |                                                                             |
| 0         | USB_SERIAL_JTAG_CONFIG_UPDATE             | Configures whether to update the value of configuration registers from APB clock domain to 48 MHz clock domain. <br> 0: No effect <br> 1: Update (WT) |

```
Espressif Systems
969
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback