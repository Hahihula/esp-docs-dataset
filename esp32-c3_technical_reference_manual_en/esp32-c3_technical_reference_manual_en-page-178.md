

```markdown
| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Configuration Registers              |                                                                             |           |        |
| IO_MUX_PIN_CTRL_REG                 | Clock output configuration Register                                       | 0x0000    | R/W    |
| IO_MUX_GPIO00_REG                   | IO MUX configuration register for pin XTAL_32K_P                          | 0x0004    | R/W    |
| IO_MUX_GPIO1_REG                    | IO MUX configuration register for pin XTAL_32K_N                          | 0x0008    | R/W    |
| IO_MUX_GPIO2_REG                    | IO MUX configuration register for pin GPIO2                               | 0x000C    | R/W    |
| IO_MUX_GPIO3_REG                    | IO MUX configuration register for pin GPIO3                               | 0x0010    | R/W    |
| IO_MUX_GPIO4_REG                    | IO MUX configuration register for pin MTMS                                | 0x0014    | R/W    |
| IO_MUX_GPIO5_REG                    | IO MUX configuration register for pin MTDI                                | 0x0018    | R/W    |
| IO_MUX_GPIO6_REG                    | IO MUX configuration register for pin MTCK                                | 0x001C    | R/W    |
| IO_MUX_GPIO7_REG                    | IO MUX configuration register for pin MTDO                                | 0x0020    | R/W    |
| IO_MUX_GPIO8_REG                    | IO MUX configuration register for pin GPIO8                               | 0x0024    | R/W    |
| IO_MUX_GPIO9_REG                    | IO MUX configuration register for pin GPIO9                               | 0x0028    | R/W    |
| IO_MUX_GPIO10_REG                   | IO MUX configuration register for pin GPIO10                              | 0x002C    | R/W    |
| IO_MUX_GPIO11_REG                   | IO MUX configuration register for pin VDD_SPI                             | 0x0030    | R/W    |
| IO_MUX_GPIO12_REG                   | IO MUX configuration register for pin SPIHD                               | 0x0034    | R/W    |
| IO_MUX_GPIO13_REG                   | IO MUX configuration register for pin SPIWP                               | 0x0038    | R/W    |
| IO_MUX_GPIO14_REG                   | IO MUX configuration register for pin SPICSO                             | 0x003C    | R/W    |
| IO_MUX_GPIO15_REG                   | IO MUX configuration register for pin SPICLK                              | 0x0040    | R/W    |
| IO_MUX_GPIO16_REG                   | IO MUX configuration register for pin SPID                                | 0x0044    | R/W    |
| IO_MUX_GPIO17_REG                   | IO MUX configuration register for pin SPIQ                                | 0x0048    | R/W    |
| IO_MUX_GPIO18_REG                   | IO MUX configuration register for pin GPIO18                              | 0x004C    | R/W    |
| IO_MUX_GPIO19_REG                   | IO MUX configuration register for pin GPIO19                              | 0x0050    | R/W    |
| IO_MUX_GPIO20_REG                   | IO MUX configuration register for pin UORXD                               | 0x0054    | R/W    |
| IO_MUX_GPIO21_REG                   | IO MUX configuration register for pin UOTXD                               | 0x0058    | R/W    |
| Version Register                    |                                                                             |           |        |
| IO_MUX_DATE_REG                     | IO MUX Version Control Register                                           | 0x00FC    | R/W    |

## 5.14.3 SDM Register Summary

The addresses in this section are relative to (GPIO base address provided in Table 3.3-3 in Chapter 3 System and Memory + 0x0F00).

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                         | Description                                                                 | Address   | Access |
|------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Configuration registers      |                                                                             |           |        |
```