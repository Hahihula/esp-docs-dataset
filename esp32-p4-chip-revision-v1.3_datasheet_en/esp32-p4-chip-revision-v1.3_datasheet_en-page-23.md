**Title:**
2 Pins

**Subtitle and Section Heading:**
2.3.3 Analog Functions

**Body Text:**
Some IO pins also have analog functions, for analog peripherals (such as touch sensor and ADC) in any power mode. Internal analog signals are routed to these analog functions; see Table 2-6 Analog Functions.

**Table Title:**
Table 2-6. Analog Signals Routed to Analog Functions

| Pin Function | Signal | Description |
|--------------|--------|-------------|
| XTAL_32K_N   | Negative clock signal | 32 kHz external clock input/output |
| XTAL_32K_P   | Positive clock signal | connected to the oscillator |
| TOUCH_CHANNEL... | Touch sensor channel signal | Touch sensor interface |
| ADC_... CHANNEL... | ADC1/2 channel signal | ADC1/2 interface |
| USB1P1_N...  | USB D- | USB 2.0 full-speed OTG interface and |
| USB1P1_P...  | USB D+ | USB Serial/JTAG function |
| ANA_COMP...   | Voltage of PO/P1 | Analog voltage comparator O/1 interface |

**Table Title:**
Table 2-7. Analog Functions

**Body Text:**
Table 2-7 shows the analog functions of IO pins.

| Pin No. | Analog Function F0 | Analog Function F1 |
|---------|--------------------|-------------------|
| 1       | GPIO1              | XTAL_32K_P        |
| 2       | GPIO2              | TOUCH_CHANNEL1    |
| 3       | GPIO3              | TOUCH_CHANNEL2    |
| 4       | GPIO4              | TOUCH_CHANNEL3    |
| 5       | GPIO5              | TOUCH_CHANNEL4    |
| 6       | GPIO6              | TOUCH_CHANNEL5    |
| 7       | GPIO7              | TOUCH_CHANNEL6    |
| 8       | GPIO8              | TOUCH_CHANNEL7    |
| 9       | GPIO9              | TOUCH_CHANNEL8    |
| 10      | GPIO10             | TOUCH_CHANNEL9    |
| 11      | GPIO11             | TOUCH_CHANNEL10   |
| 12      | GPIO12             | TOUCH_CHANNEL11   |
| 13      | GPIO13             | TOUCH_CHANNEL12   |
| 14      | GPIO14             | TOUCH_CHANNEL13   |
| 15      | GPIO15             | TOUCH_CHANNEL14   |
| 16      | GPIO16             | ADC1_CHANNEL0     |
| 17      | GPIO17             | ADC1_CHANNEL1     |
| 18      | GPIO18             | ADC1_CHANNEL2     |
| 19      | GPIO19             | ADC1_CHANNEL3     |
| 20      | GPIO20             | ADC1_CHANNEL4     |
| 21      | GPIO21             | ADC1_CHANNEL5     |
| 22      | GPIO22             | ADC1_CHANNEL6     |

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Information:**  
ESP32-P4 Series Datasheet v0.6, Page 23