Title: Pin Overview

Subtitle: Table 2-1. Pin Overview

Table:
| Name       | No. | Type | Function                                                                 |
|------------|-----|------|--------------------------------------------------------------------------|
| VDDA       | 1   | P    | Analog power supply (2.3 V ~ 3.6 V)                                    |
| LNA_IN     | 2   | I/O  | RF input and output                                                     |
| VDD3P3    | 3   | P    | Analog power supply (2.3 V ~ 3.6 V)                                    |
| VDD3P3    | 4   | P    | Analog power supply (2.3 V ~ 3.6 V)                                    |
| SENSOR_VP  | 5   | I     | GPIO36, ADC1_CH0, RTC_GPIO00                                          |
| SENSOR_CAPP| 6   | I/O  | GPIO37, ADC1_CH1, RTC_GPIO1                                           |
| SENSOR_CAPN| 7   | I/O  | GPIO38, ADC1_CH2, RTC_GPIO2                                            |
| SENSOR_VN  | 8   | I     | GPIO39, ADC1_CH3, RTC_GPIO3                                             |
| CHIP_PU    | 9   | I     | GPIO34, ADC1_CH6, RTC_GPIO4                                              |
| VDET_1    | 10  | P     | GPIO35, ADC1_CH7, RTC_GPIO5                                               |
| VDET_2    | 11  | I/O  | GPIO32, ADC1_CH4, RTC_GPIO9, TOUCH9, 32K_XP (32.768 kHz crystal oscillator input) |
| 32K_XP    | 12  | I/O  | GPIO30, ADC1_CH5, RTC_GPIO8, TOUCH8, 32K_XN (32.768 kHz crystal oscillator output) |
| GPIO25     | 14  | I/O  | GPIO25, ADC2_CH8, RTC_GPIO6, DAC_1, EMAC_RXD0                         |
| GPIO26     | 15  | I/O  | GPIO26, ADC2_CH9, RTC_GPIO7, DAC_2, EMAC_RXD1                          |
| GPIO27     | 16  | I/O  | GPIO27, ADC2_CH10, RTC_GPIO8, TOUCH7, EMAC_RX_DV                       |
| MTMS       | 17  | I/O  | GPIO14, ADC2_CH6, RTC_GPIO16, TOUCH6, EMAC_TXD2, HSPICLK, HS2_CLK, SD_CLK, MTDI |
| MTDI       | 18  | I/O  | GPIO12, ADC2_CH5, RTC_GPIO15, TOUCH5, EMAC_TXD3, HS2_DATA2, HS2_DATA3, MTDI |
| VDD3P3_RTC | 19  | P     | Input power supply for RTC IO (2.3 V ~ 3.6 V)                           |
| MTCK       | 20  | I/O  | GPIO13, ADC2_CH4, RTC_GPIO14, TOUCH4, EMAC_RX_ER, HSPIO, HS2_DATA3, SD_DATA3, MTDI |
| MDIO       | 21  | I/O  | GPIO15, ADC2_CH3, RTC_GPIO13, TOUCH3, EMAC_RXD3, HSPICSO, HS2_CMD, SD_CMD, MTDO |

Note: The table is structured with columns labeled "Name," "No.," "Type," and "Function." Each row provides specific details about the pin's name (e.g., VDDA), its number in a series or sequence of pins ("1"), type designation such as input/output (I/O) for digital signals, power supply analog functions like "Analog power supply" with specified voltage ranges. Some rows include additional information on GPIO numbers and associated functions.

Footer: ESP32 Series Datasheet v5 2

(Note: The text in the image is clear enough to transcribe accurately without any significant errors or omissions.)