**Title:**
2 Pins

**Subtitle and Body Text:**
2.3.3 Analog Functions  
Some IO pins also have analog functions, for analog peripherals (such as ADC) in any power mode. Internal analog signals are routed to these analog functions; see Table 2-5 Analog Functions.

**Table Title:**  
Table 2-5. Analog Signals Routed to Analog Functions

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| ADC1_CHn     | ADC1 channel n signal | ADC1 channel interface                          |
| XTAL_32K_N   | Negative clock signal | The differential clock input of the chip, connecting to the |
| XTAL_32K_P   | Positive clock signal | 32 kHz differential clock output of the external crystal|
| USB_D-       | USB data differential signal | USB Serial/JTAG function                         |
| USB_D+       |              |                                                |
| ZCDn         | Voltage from GPIO Pad | Analog Pad voltage comparator interface          |

**Table Title:**  
Table 2-6. Analog Functions

| Pin No. | Analog IO Name | F0   | F1    |
|---------|----------------|------|-------|
| 6       | XTAL_32K_P     | XTAL_32K_P | -      |
| 7       | XTAL_32K_N     | XTAL_32K_N | ADC1_CH0 |
| 9       | MTMS            | ADC1_CH1 |
| 10      | MTDI           | ADC1_CH2 |
| 11      | MTCK            |        |
| 28      | USB_D-         | USB_D-   | -      |
| 29      | USB_D+         | USB_D+   | -      |
| 24      | VDD_SPI        | VDD_SPI |
| 31      | GPIO8_2        | ZCDO    |
| 32      | SPIO9          |        |

**Note:**  
*Bold marks the default pin functions in the default boot mode. See Section 3.1 Chip Boot Mode Control.*

**Footer Text:**
Regarding highlighted cells, see Section 2.3.4 Restrictions for GPIOs and LP GPIOs.

**Document Footer Information:**
Espressif Systems  
ESP32-C61 Series Datasheet v0.5

**Page Number:** 
20