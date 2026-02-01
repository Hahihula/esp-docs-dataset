**Title:**
2 Pins

**Subtitle and Section Number:**
2.3.4 Analog Functions

**Body Text:**
Some IO pins also have analog functions, for analog peripherals (such as ADC) in any power mode. Internal analog signals are routed to these analog functions, see Table 2-7 Analog Signals Routed to Analog Functions.

**Table Title and Description:**
Table 2-7. Analog Signals Routed to Analog Functions

| Pin Function | Signal     | Description                                    |
|--------------|------------|------------------------------------------------|
| TOUCH...     | Touch sensor channel ... signal | Touch sensor interface                          |
| ADC..._CH... | ADC1/2 channel ... signal | ADC1/2 interface                                |
| XTAL_32K_N  | Negative clock signal | 32 kHz external clock input/output                |
| XTAL_32K_P  | Positive clock signal connected to ESP32-S2’s crystal or oscillator |
| USB_D-      | Data -    | USB OTG                                          |
| USB_D+      | Data +    | USB OTG                                          |
| DAC ...     | DAC ...   | Digital-to-Analog converter                     |

**Additional Information:**
Table 2-8 Analog Functions shows the analog functions of IO pins.

**Subsequent Table Title and Description:**
Table 2-8. Analog Functions

| Pin No. | RTC IO^1 | F0    | F1     |
|---------|----------|-------|--------|
| 6       | RTC_GPIO1 | TOUCH1 | ADC1_CH0 |
| 7       | RTC_GPIO2 | TOUCH2 | ADC1_CH1 |
| 8       | RTC_GPIO3 | TOUCH3 | ADC1_CH2 |
| 9       | RTC_GPIO4 | TOUCH4 | ADC1_CH3 |
| 10      | RTC_GPIO5 | TOUCH5 | ADC1_CH4 |
| 11      | RTC_GPIO6 | TOUCH6 | ADC1_CH5 |
| 12      | RTC_GPIO7 | TOUCH7 | ADC1_CH6 |
| 13      | RTC_GPIO8 | TOUCH8 | ADC1_CH7 |
| 14      | RTC_GPIO9 | TOUCH9 | ADC1_CH8 |
| 15      | RTC_GPIO10 | TOUCH10 | ADC1_CH9 |
| 16      | RTC_GPIO11 | TOUCH11 | ADC2_CH0 |
| 17      | RTC_GPIO12 | TOUCH12 | ADC2_CH1 |
| 18      | RTC_GPIO13 | TOUCH13 | ADC2_CH2 |
| 19      | RTC_GPIO14 | TOUCH14 | ADC2_CH3 |
| 20      | RTC_GPIO15 | XTAL_32K_P | XTAL_32K_N |
| 21      | RTC_GPIO16 | XTAL_32K_N | XTAL_32K_N |
| 22      | RTC_GPIO17 | DAC_1   | ADC2_CH4 |
| 23      | RTC_GPIO18 | DAC_2   | ADC2_CH5 |
| 24      | RTC_GPIO19 | USB_D-  | ADC2_CH6 |
| 25      | RTC_GPIO20 | USB_D+  | ADC2_CH7 |

**Footer Note:**
This column lists the RTC GPIO names, since analog functions are configured with RTC GPIO registers that use RTC GPIO numbering.

^ Regarding highlighted cells, see Section 2.3.5 Restrictions for GPIOs and RTG PIOs

**Document Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Page Numbering:**
21 ESP32-S2 Series Datasheet v1.8