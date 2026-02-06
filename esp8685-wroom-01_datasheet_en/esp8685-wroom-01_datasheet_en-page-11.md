**Title:**
3 Pin Definitions

**Subtitle:**
For peripheral pin configurations, please refer to ESP8685 Series Datasheet.

**Table Title:**
Table 3-1. Pin Definitions

| Name | No. | Type^1 | Function |
|------|-----|--------|----------|
| IO0  | 1   | I/O/T  | GPIO0, ADC1_CH0, XTAL_32K_P |
| IO1  | 2   | I/O/T  | GPIO1, ADC1_CH1, XTAL_32K_N |
| EN   | 3   | I     | High: on, enables the chip. Low: off, the chip powers off. By default, this pin is internally pulled high. |
| IO2  | 4   | I/O/T  | GPIO2, ADC1_CH2, FSPIQ |
| IO4  | 5   | I/O/T  | GPIO4, ADC1_CH4, FSPIHD, MTMS, LED PWM |
| IO5  | 6   | I/O/T  | GPIO5, ADC2 CHO, FSPIWP, MTDI, LED PWM |
| IO6  | 7   | I/O/T  | GPIO6, FSPICLK, MTCK, LED PWM |
| 3V3  | 8   | P     | Power supply |
| IO18 | 9   | I/O/T  | GPIO18, USB_D- |
| IO19 | 10  | I/O/T  | GPIO19, USB_D+ |
| NC   | 11-14 | —      | NC       |
| GND  | 15,23| P     | Ground   |
| IO7  | 16  | I/O/T  | GPIO7, FSPID, MTDO, LED PWM |
| IO8  | 17  | I/O/T  | GPIO8    |
| IO9  | 18  | I/O/T  | GPIO9    |
| IO10 | 19  | I/O/T  | GPIO10, FSPICS0, LED PWM |
| IO3  | 20  | I/O/T  | GPIO3, ADC1_CH3, LED PWM |
| RXD0 | 21  | I/O/T  | GPIO20, UORXD |
| TXD0 | 22  | I/O/T  | GPIO21, UOTXD |

**Footnote:**
^1 P: power supply; I: input; O: output; T: high impedance.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP8685-WROOM-01 Datasheet v1.5