**Title:**
2 Pins

**Subtitle and Section Number:**
2.3.2 Analog Functions

**Body Text:**
Some IO pins also have analog functions, for analog peripherals (such as ADC) in any power mode. Internal analog signals are routed to these analog functions, see Table 2-5 Analog Signals Routed to Analog Functions.

**Table Title and Description:**
Table 2-5. Analog Signals Routed to Analog Functions

| Pin Function | Signal   | Description |
|--------------|----------|-------------|
| ADC..._CH... | ADC1/2 channel ... signal | ADC1/2 interface |
| USB_D-       | Data -    | USB Serial/JTAG function |
| USB_D+       | Data +    |          |
| XTAL_32K_N  | Negative clock signal | 32 kHz external clock input/output |
| XTAL_32K_P  | Positive clock signal | connected to ESP32-C3’s crystal or oscillator |

**Additional Information:**
Table 2-6 Analog Functions shows the analog functions of IO pins.

**Table Title and Description for Table 2-6:**
Table 2-6. Analog Functions

| Pin No. | Analog IO Name | Analog Function F1 |
|---------|---------------|--------------------|
| 4       | GPIO0         | ADC1_CH0           |
| 5       | GPIO1         | ADC1_CH1           |
| 6       | GPIO2         | ADC1_CH2           |
| 8       | GPIO3         | ADC1_CH3           |
| 9       | GPIO4         | ADC1_CH4           |
| 10      | GPIO5         | ADC2_CH0           |
| 25      | GPIO18        | USB_D-             |
| 26      | GPIO19        | USB_D+             |

**Footnote:**
1. Bold marks the default pin functions in the default boot mode.
2. Regarding highlighted cells, see Section 2.3.3 Restrictions for GPIOs.

**Footer Information:**
Espressif Systems
ESP32-C3 Series Datasheet v2.2

**Link Text at Bottom of Page:**
Submit Documentation Feedback