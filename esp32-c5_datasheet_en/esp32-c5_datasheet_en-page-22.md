**Title:**
2 Pins

**Subtitle and Section Heading:**
2.3.3 Analog Functions

**Body Text:**
Some IO pins also have analog functions, for analog peripherals (such as ADC) in any power mode. Internal analog signals are routed to these analog functions, see Table 2-6 Analog Signals Routed to Analog Functions.

**Table Title and Description:**
Table 2-6. Analog Signals Routed to Analog Functions

| Pin Function | Signal   | Description                  |
|--------------|----------|------------------------------|
| ADC1_CH...   | ADC1 channel ... signal | ADC1 interface               |
| XTAL_32K_N  | Negative clock signal    | 32 kHz external clock input/output |
| XTAL_32K_P  | Positive clock signal    | connected to ESP32-C5's oscillator |
| USB_D-      | Data -                   | USB Serial/JTAG function     |
| USB_D+      | Data +                   |                               |
| PAD_COMP...  | PAD... signal           | Analog voltage comparator input |

**Additional Information:**
Table 2-7 Analog Functions shows the analog functions of IO pins.

**Subsection Title and Table Description:**
Table 2-7. Analog Functions

| QFN48 Pin No. | Analog IO Name   | Analog Function1,2 F0    | F1 |
|---------------|------------------|-------------------------------|
| 9             | GPIO0            | XTAL_32K_P                   |    |
| 10            | GPIO1            | XTAL_32K_N                   | ADC1_CH0 |
| 11            | GPIO2            |                              |        |
| 12            | GPIO3            |                              |        |
| 13            | GPIO4            |                              |        |
| 14            | GPIO5            |                              |        |
| 15            | GPIO6            |                              |        |
| 17            | GPIO8            | PAD_COMP0                    |        |
| 18            | GPIO9            | PAD COMP1                    | USB_D- |
| 22            | GPIO13           |                              | USB_D+ |
| 23            | GPIO14           |                              | VDD_SPI|
| 29            | GPIO19           |                              |        |

**Footnotes:**
1. Bold marks the default pin functions in SPI Boot mode.
2. Regarding highlighted cells, see Section 2.3.4 Restrictions for GPIOs and LP GPIOs.

**Footer Information:**
Espressif Systems
ESP32-C5 Series Datasheet v1.0

**Link Text at Bottom of Page:**
Submit Documentation Feedback