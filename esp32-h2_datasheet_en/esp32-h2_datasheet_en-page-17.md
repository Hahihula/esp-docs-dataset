**Title:**
2 Pins

**Subtitle and Body Text:**

**2.3.2 Analog Functions**

Some IO pins also have analog functions, for analog peripherals (such as ADC) in any power mode. Internal analog signals are routed to these analog functions, see Table 2-4 Analog Signals Routed to Analog Functions.

**Table Title:**  
Table 2-4. Analog Signals Routed to Analog Functions

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| ADC1_CHn     | ADC1 channel n signal | ADC1 channel n interface                       |
| XTAL_32K_N   | Negative clock signal | 32 kHz external clock input/output              |
| XTAL_32K_P   | Positive clock signal | connected to ESP32-H2’s oscillator/crystal     |
| USB_D-       | Data - (negative USB signal) | USB signals from USB Serial/JTAG Controller    |
| USB_D+       | Data + (positive USB signal) |                                          |
| ZCDn         | Voltage from GPIO Pad | Analog Pad voltage comparator interface        |

**Table Title:**  
Table 2-5. Analog Functions

| Pin No. | Analog IO Name^1 | Analog Function^2 F0 | Analog Function^2 F1 |
|---------|------------------|----------------------|----------------------|
| 4       | GPIO1            | ADC1_CH10           |                     |
| 5       | GPIO2            | ADC1_CH11           |                     |
| 6       | GPIO3            | ADC1_CH12           |                     |
| 7       | GPIO4            | ADC1_CH13           |                     |
| 8       | GPIO5            | ADC1_CH14           |                     |
| 9       |                  |                      |                     |
| 10      |                  |                      |                     |
| 12      | GPIO10           | ZCDO                 |                     |
| 13      | GPIO11           | ZCD1                 |                     |
| 15      | XTAL_32K_P       | XTAL_32K_P          |                     |
| 16      | XTAL_32K_N       | XTAL_32K_N          |                     |
| 25      | GPIO26           | USB_D-              |                     |
| 26      | GPIO27           | USB_D+              |                     |

^1 Bold marks the default pin functions in the default boot mode. See Section 3.1 Chip Boot Mode Control.

^2 Regarding highlighted cells, see Section 2.3.3 Restrictions for GPIOs

**Footer:**
Espressif Systems  
Submit Documentation Feedback  

**Page Number:** 
17