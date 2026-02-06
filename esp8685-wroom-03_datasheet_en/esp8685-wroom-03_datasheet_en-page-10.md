Title: Pin Definitions

Subtitle: 3.1 Pin Layout

Body Text:
The pin diagram below shows the approximate location of pins on the module. For the actual diagram drawn to scale, please refer to Figure 10 Module Dimensions.

Image Description (Figure Caption):
- Title: "Pin Layout (Top View and Bottom View)"
- The image is a schematic representation showing two views labeled as Top View and Bottom View with various pin labels such as EN, IO1 through IO9. There are also annotations like Keepout Zone on both sides of the diagram.

Note:
- Note A states that “The zone marked with dotted lines is the antenna keepout zone.” It advises to refer to ESP32-C3 Hardware Design Guidelines > Section General Principles of PCB Layout for Modules.
  
Subtitle: 3.2 Pin Description

Body Text:
The module has 11 pins. See pin definitions in Table 3-1.

For peripheral pin configurations, please refer to ESP8685 Series Datasheet.

Table Title (Table Caption):
- "Table 3-1. Pin Definitions"

Table Content:

| Name | No. | Type^1 | Function |
|------|-----|--------|----------|
| EN   | 1   | I      | High: on, enables the chip. Low: off, the chip powers off. Default: internally pulled-up |
| IO1  | 2   | I/O/T  | GPIO1, ADC1_CH1, XTAL_32K_N |
| IO6  | 3   | I/O/T  | GPIO6, FSPICLK, MTCK, LED PWM |
| IO7  | 4   | I/O/T  | GPIO7, FSPID, MTD0, LED PWM |
| IO3  | 5   | I/O/T  | GPIO3, ADC1_CH3, LED PWM |

Footer:
- "Espressif Systems"
- Page number: “10”
- Document version and feedback link text at the bottom right corner reads as follows:

ESP8685-WROOM-03 Datasheet v1.5
Submit Documentation Feedback