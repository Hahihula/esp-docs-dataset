**Title: ESP32 Datasheet v5.2**

**Table of Pin Descriptions:**

| Name       | No.   | Type    | Function                                    |
|------------|-------|---------|----------------------------------------------|
| GPIO0      | 18    | I/O     | ADC2_CH2, RTC_GPIO12, TOUCH2                |
| GPIO16     | 25    | I/O     | GPIO16, HS1_DATA4, U2RXD                    |
| VDD_SDIO   | -     | P       | Output power supply: 1.8 V or the same voltage as VDD3P3_RTC |
| GPIO17     | 27    | I/O     | GPIO17, HS1_DATA5, U2TXD                    |
| SD_DATA_2 | 28    | I/O     | GPIO9, HS1_DATA2, U1RXD                     |
| SD_DATA_3 | 29    | I/O     | GPIO10, HS1_DATA3, U1TXD                    |
| SD_CMD     | 30    | I/O     | GPIO11, HS1_CMD, U1RTS                      |
| SD_CLK     | 31    | I/O     | GPIO6, HS1_CLK, U1CTS                       |
| SD_DATA_0 | 32    | I/O     | GPIO7, HS1_DATAO, U2RTS                     |
| SD_DATA_1 | 33    | I/O     | GPIO8, HS1_DATA1, U2CTS                     |
| GPIO5      | 34    | I/O     | GPIO5, HS1_DATA6, VSPICSO                   |
| GPIO18     | 35    | I/O     | GPIO18, HS1_DATA7, VSPICLK                  |
| GPIO23     | 36    | I/O     | GPIO23, HS1_STROBE, VSPID                   |
| VDD3P3_CPU | -     | P       | Input power supply for CPU IO (1.8 V ~ 3.6 V)|
| GPIO19     | 38    | I/O     | GPIO19, U0CTS, VSPIQ                        |
| GPIO22     | 39    | I/O     | GPIO22, U0RTS, VSPIWD                      |
| UORX        | -     | P       | Clock output for CPU IO (1.8 V ~ 3.6 V)      |
| UOTXD       | 41    | I/O     | GPIO1, UOTXD, CLK_OUT3                      |
| GPIO21     | 42    | I/O     | GPIO21, VSPIHD, EMAC_TX_EN                 |

**Analog Section:**

- VDDA (43): Analog power supply (2.3 V ~ 3.6 V)
- XTAL_N (44): External crystal output
- XTAL_P (45): External crystal input
- VDDA (46): Analog power supply (2.3 V ~ 3.6 V)

**Additional Notes:**

- CAP2 (47): Connects to a 3.3 nF (10%) capacitor and 20 kΩ resistor in parallel to CAP1

(Note: The table includes additional rows with descriptions that are not fully visible, hence they have been omitted.)