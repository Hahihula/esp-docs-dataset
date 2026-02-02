**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Subtitle:**
6.10 IO MUX Pin List

**Body Text:**

Table 6.10-1 shows the IO MUX functions for each I/O pin:

| GPIO | Pin Name | Function 0 | Function 1 | Function 2 | Function 3 | Function 4 | Function 5 | Reset | Notes |
|------|----------|------------|------------|------------|------------|-----------|---------|-------|-------|
| O    | GPIO0    | GPIO0      | CLK_OUT_1 | GPIO0      | -          | -         | EMAC_TX_CLK | 3     | R     |
| 1    | UOTXD    | UOTXD      | CLK_OUT_3 | GPIO1      | -          | -         | EMAC_RXD2   | 3     | -     |
| 2    | GPIO2    | GPIO2      | HSPIWP    | GPIO2      | HS2_DATA0 | SD_DATA0   | -         | 2     | R     |
| 3    | UORXD    | UORXD      | CLK_OUT_2 | GPIO3      | -          | -         | EMAC_TX_ER  | 3     |       |
| 4    | GPIO4    | GPIO4      | HSPIHD    | GPIO4      | HS2_DATA1 | SD_DATA1   | EMAC_RX_CLK | 2     | R     |
| 5    | GPIO5    | GPIO5      | VSPICSO0  | GPIO5      | HS1_DATA6 | -         | -         |       |       |
| 6    | SD_CLK   | SD_CLK     | SPICLK    | GPIO6      | HS1_CLK   | UICT5     | -         | 3     |       |
| 7    | SD_DATA_0| SD_DATA0   | SPIQ      | GPIO7      | HS1_DATA0 | U2RTS     | -         | 3     |       |
| 8    | SD_DATA_1| SD_DATA1   | SPID      | GPIO8      | HS1_DATA1 | U2CTS     | -         | 3     |       |
| 9    | SD_DATA_2| SD_DATA2   | SPIHD     | GPIO9      | HS1_DATA2 | UIRXD0    | -         | 3     |       |
| 10   | SD_DATA_3| SD_DATA3   | SPIGPIO0  | GPIO10     | HS1_DATA3 | UTXD      | -         | 3     |       |
| 11   | SD_CMD   | SD_CMD     | SPICSO    | GPIO11     | HS1_CMD   | UIRTS     | -         | 3     |       |
| 12   | MTDI     | MTDI       | HSPIQ     | GPIO12     | HS2_DATA2 | SD_DATA2   | EMAC_TXD3   | 2     | R     |
| 13   | MTCK     | MTCK       | HSPID     | GPIO13     | HS2_DATA3 | SD_DATA3   | EMAC_RX_ER  | 2     | R     |
| 14   | MTMS     | MTMS       | HSPICLK   | GPIO14     | HS2_CLK   | SD_CLK    | EMAC_TXD2   | 3     | R     |
| 15   | MTDO     | MTDO       | HSPICSO0  | GPIO15     | HS2_CMD   | SD_DATA0   | EMAC_RXD3   | 3     | R     |
| 16   | GPIO16   | GPIO16     | -         | GPIO16     | HS1_DATA4 | U2RXD      | EMAC_CLK_OUT| 1     |       |
| 17   | GPIO17   | GPIO17     | -         | GPIO17     | HS1_DATA5 | UTXD      | EMAC_CLK_180| 1     |       |
| 18   | GPIO18   | GPIO18     | VSPICLK   | GPIO18     | HS1_DATA7 | -         | -         | 1     |       |
| 19   | GPIO19   | GPIO19     | VSPIQ     | GPIO19     | UOCTS     | -         | EMAC_TXDO   | 1     |       |
| 20   | GPIO21   | GPIO21     | VSPIDH    | GPIO21     | HS1_TX_EN | -         | EMAC_TXEN   | 1     |       |
| 21   | GPIO22   | GPIO22     | SPIWP     | GPIO22     | UORTS     | -         | EMAC_TXDI   | 1     |       |
| 22   | GPIO23   | GPIO23     | VSPID     | GPIO23     | HS1_STROBE| -         | EMAC_RXDO   | O     | R     |
| 25   | GPIO25   | GPIO25     | -         | GPIO25     | -         | -         | EMAC_RXDI   | O     |       |
| 26   | GPIO26   | GPIO26     | -         | GPIO26     | -         | -         | EMAC_RX_DV  | R     |       |
| 27   | GPIO27   | GPIO27     | -         | GPIO27     | -         | -         | EMAC_RX_DY  | O     | R     |
| 32   | 32K_XP   | 32K_XP     | -         | 32K_XP     | -         | -         | -         |       |       |
| 33   | 32K_XN   | 32K_XN     | -         | 32K_XN     | -         | -         | -         | O     | R     |
| 34   | VDET_1   | VDET_1     | -         | VDET_1     | -         | -         | -         |       |       |
| 35   | VDET_2   | VDET_2     | -         | VDET_2     | -         | -         | -         | O     | R, I |
| 36   | SENSOR_VP | SENSOR_VP  | -         | SENSOR_VP  | -         | -         | -         |       |       |
| 37   | SENSOR_CAPP| SENSOR_CAPP| -        | SENSOR_CAPP| -        | -         | -         | O     | R, I |
| 38   | SENSOR_CAPN| SENSOR_CAPN| -        | SENSOR_CAPN| -        | -         | -         |       |       |
| 39   | SENSOR_VN | SENSOR_VN  | -         | SENSOR_VN  | -         | -         | -         | O     | R, I |

**Reset Configurations:**

"Reset" column shows each pin's default configurations after reset:
- **0**: IE=0 (input disabled).
- **1**: IE=1 (input enabled).
- **2**: IE=1, WPD=1 (input enabled, pull-down resistor).
- **3**: IE=1, WPU=1 (input enabled, pull-up resistor).

**Notes:**

- R - Pin has RTC/analog functions via RTC_MUX.

Espressif Systems

ESP32 TRM (Version 5.6)

Submit Documentation Feedback