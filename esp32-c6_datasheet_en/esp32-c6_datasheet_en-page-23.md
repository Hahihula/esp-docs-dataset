**Title:**
2 Pins

**Subtitle and Body Text:**
2.3.3 Analog Functions  
Some IO pins also have analog functions, for analog peripherals (such as ADC) in any power mode. Internal analog signals are routed to these analog functions, see Table 2-8 Analog Signals Routed to Analog Functions.

**Table Title:**  
Table 2-8. Analog Signals Routed to Analog Functions

| Pin Function | Signal   | Description |
|--------------|----------|-------------|
| ADC1_CH...   | ADC1 channel ... signal | ADC1 interface |
| XTAL_32K_N  | Negative clock signal | 32 kHz external clock input/output |
| XTAL_32K_P  | Positive clock signal | connected to ESP32-C6's crystal or oscillator |
| USB_D-      | Data -   | USB Serial/JTAG function |
| USB_D+      | Data +   | |

**Table Title:**  
Table 2-9. Analog Functions

| QFN40 | QFN32 | Analog IO Name | Analog Function |
|-------|-------|---------------|----------------|
| Pin No. | Pin No. | I/O Name       | F0             | F1            |
| 6      | 6     | GPIO0         | XTAL_32K_P    | ADC1_CH0      |
| 7      | 7     | GPIO1         | XTAL_32K_N    | ADC1_CH1      |
| 8      | 8     | GPIO2         |               | ADC1_CH2      |
| 9      | 9     | GPIO3         |               | ADC1_CH3      |
| 10     | 10    | GPIO4         |               | ADC1_CH4      |
| 11     | 11    | GPIO5         |               | ADC1_CH5      |
| 12     | 12    | GPIO6         |               | ADC1_CH6      |
| 18     | 17    | GPIO12        | USB_D-        |              |
| 19     | 18    | GPIO13        | USB_D+        |              |
| 23     | 20    | GPIO27        | VDD_SPI        |              |

**Footnotes:**
1. Bold marks the default pin functions in the default boot mode.
2. Regarding highlighted cells, see Section 2.3.4 Restrictions for GPIOs and LP GPIOs.

**Footer:**  
Espressif Systems  
ESP32-C6 Series Datasheet v1.4

**Link Text:**
Submit Documentation Feedback