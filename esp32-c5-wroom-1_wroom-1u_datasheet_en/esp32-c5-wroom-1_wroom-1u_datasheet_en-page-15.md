**Title: Pin Definitions**

---

**Table Title:** Table 3-2 – cont'd from previous page

| Name | No. | Type^2 | Function |
|------|-----|--------|----------|
| IO7  | 9   | I/O/T  | GPIO7, FSPID, SDIO_DATA1 |
| IO8  | 10  | I/O/T  | GPIO8, PAD_COMP0, SDIO_DATA0 |
| IO9  | 11  | I/O/T  | GPIO9, PAD_COMP1, SDIO_CLK |
| IO10 | 12  | I/O/T  | GPIO10, FSPICSO, SDIO_CMD |
| IO13 | 13  | I/O/T  | GPIO13, USB_D-, SDIO_DATA3 |
| IO14 | 14  | I/O/T  | GPIO14, USB_D+, SDIO_DATA2 |
| IO28 | 15  | I/O/T  | GPIO28 |
| IO5  | 16  | I/O/T  | MTD0, GPIO5, LP_GPIO5, LP_UART_TXD, ADC1_CH4, FSPIWP |
| IO4  | 17  | I/O/T  | MTCK, GPIO4, LP_GPIO4, LP_UART_RXD, ADC1_CH3, FSPIHD |
| IO27 | 18  | I/O/T  | GPIO27 |
| NC/IO15 | 19 | I/O/T | SPIC1S, GPIO15^3 |
| NC   | 20  | -      | NC       |
| IO23 | 21  | I/O/T  | GPIO23 |
| NC   | 22  | -      | NC       |
| IO24 | 23  | I/O/T  | GPIO24 |
| RXO  | 24  | I/O/T  | U0RXD, GPIO12 |
| TXO  | 25  | I/O/T  | U0TXD, GPIO11 |
| IO25 | 26  | I/O/T  | GPIO25 |
| IO26 | 27  | I/O/T  | GPIO26 |
| GND  | 28  | P      | Ground   |
| EPAD | 29  | P      | Ground   |
| GND  | 30  | P      | Ground   |
| ANT2^4 | 31 | I/O    | RF input and output |
| GND  | 32  | P      | Ground   |

**Footnotes:**
- ^2 P: power supply; I: input; O: output; T: high impedance.
- ^3 In modules with the in-package SPI PSRAM, this pin is used as SPIC1 for SPI PSRAM and cannot be used for other functions; in modules without the in-package SPI PSRAM, this pin can be used as GPIO15.

**Additional Note:** By default, ESP32-C5-WROOM-1U uses ANT1, and ANT2 is disabled. To use ANT2, please [contact us](#).

---

**Footer:**
Espressif Systems  
Page 15 ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8  
Submit Documentation Feedback  
PRELIMINARY