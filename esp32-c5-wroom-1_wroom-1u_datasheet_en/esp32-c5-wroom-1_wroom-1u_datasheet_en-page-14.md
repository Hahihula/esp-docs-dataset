**Title: Pin Definitions**

---

### Table-3 (continued from previous page)

| Name | No. | Type^2 | Function |
|------|-----|--------|----------|
| IO03 | 5   | I/O/T  | MTDI, GPIO3, LP_UART_CTSN, LP_I2C_SCL, ADC1_CH2 |
| IO06 | 7   | I/O/T  | GPIO1, XTAL_32K_N, LP_GPI00, LP_UART_DSTRN, ADC1_CHO |
| IO08 | 9   | I/O/T  | GPIO7, LP_GPIO7, FSPID, SDIO_DATA1 |
| IO09 | 11  | I/O/T  | GPIO9, PAD_COMP1, SDIO_CLK |
| IO13 | 14  | I/O/T  | USB_D-, SDIO_DATA3 |
| IO28 | 15  | I/O/T  | GPIO28 |
| IO07 | 16  | I/O/T  | MTDO, GPIO5, LP_UART_TXD, ADC1_CH4, FSPIWP |
| IO27 | 19  | I/O/T  | GPIO27 |
| NC/IO15 | - | I/O/T | SPICS1, GPIO15^3 |
| NC   | 20  | -      | NC       |
| IO23 | 21  | I/O/T  | GPIO23 |
| NC   | 22  | -      | NC       |
| IO24 | 23  | I/O/T  | GPIO24 |
| RXO  | 25  | I/O/T  | UORXD, GPIO12 |
| TXO  | 26  | I/O/T  | UOTXD, GPIO11 |
| IO25 | 27  | I/O/T  | GPIO25 |
| GND  | -   | P      | Ground   |
| EPAD | 29  | P      | Ground   |

^1 This table shares the notes 2 and 3 presented in Table-3 below.

---

### Table-3. ESP32-C5-WROOM-1U Pin Definitions

| Name | No. | Type^2 | Function |
|------|-----|--------|----------|
| GND  | 1   | P      | Ground   |
| 3V3  | 2   | P      | Power Supply |
| EN   | 3   | I      | High: on, enables the chip. Low: off, the chip powers off. Note: Do not leave the EN pin floating. |
| IO02 | 4   | I/O/T  | MTMS, GPIO2, LP_GPIO2, LP_UART_RTSN, LP_I2C_SDA, ADC1_CH1, FSPIQ |
| IO03 | 5   | I/O/T  | MTDI, GPIO3, LP_GPIO3, LP_UART_CTSN, LP_I2C_SCL, ADC1_CH2 |
| IO06 | 7   | I/O/T  | GPIO1, XTAL_32K_N, LP_GPI00, LP_UART_DSTRN |
| IO09 | 8   | I/O/T  | GPIO6, LP_GPIO6, ADC1_CH5, FSPICLK |

---

**Footer:**
Espressif Systems
Page number and document information at the bottom.