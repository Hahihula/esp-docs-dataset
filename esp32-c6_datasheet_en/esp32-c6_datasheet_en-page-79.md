Title: ESP32-C6 Consolidated Pin Overview

Table Title: Table 7-1. QFN40 Pin Overview

| Pin No | Pin Name | Type   | Power | At Reset | Analog Function | IO MUX Function       |
|--------|----------|--------|-------|-----------|------------------|-----------------------|
|        |          |        |       |           |                  |                       |
| 1      | ANT      | Analog |       |           |                  |                      |
| 2      | VDDA3P3 | Power  |       |           |                  |                      |
| 3      | VDDA3P3 | Power  |       |           |                  |                      |
| 4      | CHIP PU | Analog |       |           |                  |                      |
| 5      | VDDPST1 | Power  |       |           |                  |                      |
| 6      | XTAL_32K_P | IO   | VDDPST1 |          | ADC1_CH0         | LP_GPIO0              | GPIO0                 |
| 7      | XTAL_32K_N | IO    | VDDPST1 |          | ADC1_CH1         | LP_UART_DTRN         | GPIO1                 |
|        |          |        |       |           |                  |                      |
| ...    | ...      | ...    | ...   | ...       | ...              | ...                   | ...                   |

(Note: The table continues with similar structure for other pin numbers, but the text is truncated and not fully visible in this image. Each row follows a consistent format as shown above.)

Footer:
- "* For details, see Section 2 Pins Regarding highlighted cells, see Section 2.3.4 Restrictions for GPIOs and LP GPIOs."

(Note: The footer contains additional information about where to find more detailed descriptions of the table content.)