**Title: Pin Definitions**

---

### Table 3 – cont’d from previous page

| Name       | No.   | Type^2    | Function                                    |
|------------|-------|-----------|---------------------------------------------|
| IO12       | 17    | I/O/T     | GPIO12, USB_D-                              |
| IO13       | 18    | I/O/T     | GPIO13, USB_D+                              |
| IO29       | 19    | I/O/T     | GPIO29                                      |
| IO24       | 20    | I/O/T     | GPIO24                                      |
| NC/IO14    | 21    | I/O/T     | SPICS1, GPIO14^3                            |
| IO8        | 22    | I/O/T     | GPIO8, FSPICSO, ZCDO                        |
| IO9        | 23    | I/O/T     | GPIO9, ZCD1                                  |
| IO25       | 24    | I/O/T     | GPIO25, SDIO_CMD                            |
| IO26       | 25    | I/O/T     | GPIO26, SDIO_CLK                            |
| IO27       | 26    | I/O/T     | GPIO27, SDIO_DATA0                           |
| IO28       | 27    | I/O/T     | GPIO28, SDIO_DATA1                           |
| IO22       | 28    | I/O/T     | GPIO22, SDIO_DATA2                           |
| IO23       | 29    | I/O/T     | GPIO23, SDIO_DATA3                           |
| RXO        | 30    | I/O/T     | UORXD, GPIO10                                |
| TXO        | 31    | I/O/T     | UOTXD, GPIO11                                |

^This table shares the notes 2 and 3 presented in Table 4 below.

---

### Table 4: ESP32-C61-MINI-1U Pin Definitions

| Name       | No.   | Type^2    | Function                                    |
|------------|-------|-----------|---------------------------------------------|
| GND        | 1, 2, 11, 14, 36~43, 45~53 | P     | Ground                                      |
| 3V3        | 3     | P         | Power supply                                |
| NC         | 4, 7, 32~35       | —      | NC                                           |
| IO2        | 5     | I/O/T     | GPIO2, LP_GPIO2, FSPIQ                       |
| IO3        | 6     | I/O/T     | MTMS, GPIO3, LP_GPIO3, ADC1_CH1, FSPIHD    |
| EN         | 8     | I       | High: on, enables the chip.                  |
|           |      |          | Low: off, the chip powers off.               |
| Note: do not leave the EN pin floating.        |
| IO4        | 9     | I/O/T     | MTDI, GPIO4, LP_GPIO4, ADC1_CH2, FSPIWP     |
| IO5        | 10    | I/O/T     | MTCK, GPIO5, LP_GPIO5, ADC1_CH3              |
| IO0        | 12    | I/O/T     | GPIO0, XTAL_32K_P, LP_GPIO0                  |
| IO1        | 13    | I/O/T     | GPIO1, XTAL_32K_N, LP_GPIO1, ADC1_CH0        |
| IO6        | 15    | I/O/T     | MTDI, GPIO6, LP_GPIO6, FSPICLK               |
| IO7        | 16    | I/O/T     | FSPID                                      |
| IO12       | 17    | I/O/T     | GPIO12, USB_D-                              |
| IO13       | 18    | I/O/T     | GPIO13, USB_D+                              |
| IO29       | 19    | I/O/T     | GPIO29                                      |
| IO24       | 20    | I/O/T     | GPIO24                                      |
| NC/IO14    | 21    | I/O/T     | SPICS1, GPIO14^3                            |
| IO8        | 22    | I/O/T     | FSPICSO, ZCDO                               |
| IO9        | 23    | I/O/T     | ZCD1                                        |

---

**Footer:**
Espressif Systems
ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6

Submit Documentation Feedback