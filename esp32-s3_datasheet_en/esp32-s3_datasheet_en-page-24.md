**Title:**
2 Pins

**Subtitle and Body Text:**

**2.3.3 Analog Functions**

Some IO pins also have analog functions, for analog peripherals (such as ADC) in any power mode. Internal analog signals are routed to these analog functions, see Table 2-7 Analog Signals Routed to Analog Functions.

**Table Title:**  
Table 2-7. Analog Signals Routed to Analog Functions

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| TOUCH...     | Touch sensor channel ... signal | Touch sensor interface                          |
| ADC..._CH... | ADC1/2 channel ... signal | ADC1/2 interface                                |
| XTAL_32K_N  | Negative clock signal | 32 kHz external clock input/output                |
| XTAL_32K_P  | Positive clock signal connected to ESP32-S3's oscillator |
| USB_D-       | Data -      | USB OTG and USB Serial/JTAG function             |
| USB_D+       | Data +      |                                                |

**Table Title:**  
Table 2-8. Analog Functions

| Pin No. | GPIO | F0   | F1    |
|---------|------|------|-------|
| 6       | RTC_GPIO1 | TOUCH1 | ADC1_CH0 |
| 7       | RTC_GPIO2 | TOUCH2 | ADC1_CH1 |
|         |      |      |        |
| 9       | RTC_GPIO3 | TOUCH4 | ADC1_CH3 |
| 10      | RTC_GPIO5 | TOUCH5 | ADC1_CH4 |
| 11      | RTC_GPIO6 | TOUCH6 | ADC1_CH5 |
| ...     | ...  | ...   | ...    |
|         |      |      |        |
| 24      | RTC_GPIO18 |          | ADC2_CH7 |
| 25      | RTC_GPIO19 |          | ADC2_CH8 |
| 26      | RTC_GPIO20 |          | USB_D-   |

**Footnotes:**
1. Bold marks the default pin functions in the default boot mode.
2. This column lists the RTC GPIO names, since analog functions are configured with RTC GPIO registers that use RTC GPIO numbering.

**Additional Information:**  
Regarding highlighted cells, see Section 2.3.4 Restrictions for GPIOs and RTGPIOs

**Footer:**
Espressif Systems  
Submit Documentation Feedback  

**Document Reference:**  
ESP32-S3 Series Datasheet v2.1