

```markdown
## Register 38.7. TWAIFD_TRV_DELAY_SSP_CFG_REG (0x0080)

| Bit | Field Name               | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  |                          | (reserved)                                                                  |
| 26  |                          | (reserved)                                                                  |
| 25  |                          | (reserved)                                                                  |
| 24  | TWAIFD_SSP_SRC           | Represents the source of secondary sampling point.                           |
|     |                          | 0: SSP_SRC_MEAS_NO_OFFSET - SSP position = TRV_DELAY (measured transmitter delay) + SSP_OFFSET.<br>1: SSP_SRC_NO_SSP - SSP is not used. Transmitter uses the regular sampling point during data bit rate.<br>2: SSP_SRC_OFFSET - SSP position = SSP_OFFSET. Measured transmitter delay is ignored. (R/W) |
| 23  |                          | (reserved)                                                                  |
| 22  |                          | (reserved)                                                                  |
| 21  |                          | (reserved)                                                                  |
| 20  |                          | (reserved)                                                                  |
| 19  | TWAIFD_SSP_OFFSET        | Represents the secondary sampling point offset in multiples of the minimum time quantum. (R/W) |
| 18  |                          | (reserved)                                                                  |
| 17  |                          | (reserved)                                                                  |
| 16  |                          | (reserved)                                                                  |
| 15  |                          | (reserved)                                                                  |
| 14  |                          | (reserved)                                                                  |
| 13  |                          | (reserved)                                                                  |
| 12  |                          | (reserved)                                                                  |
| 11  |                          | (reserved)                                                                  |
| 10  |                          | (reserved)                                                                  |
| 9   |                          | (reserved)                                                                  |
| 8   |                          | (reserved)                                                                  |
| 7   |                          | (reserved)                                                                  |
| 6   |                          | (reserved)                                                                  |
| 5   |                          | (reserved)                                                                  |
| 4   |                          | (reserved)                                                                  |
| 3   |                          | (reserved)                                                                  |
| 2   |                          | (reserved)                                                                  |
| 1   |                          | (reserved)                                                                  |
| 0   | TWAIFD_TRV_DELAY_VALUE   | Represents the measured transmitter delay in multiples of the minimum time quantum. (RO) |

## Register 38.8. TWAIFD_TIMER_CLK_EN_REG (0xFD4)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                      | (reserved)                                                                  |
| 30  |                                      | (reserved)                                                                  |
| 29  |                                      | (reserved)                                                                  |
| 28  |                                      | (reserved)                                                                  |
| 27  |                                      | (reserved)                                                                  |
| 26  |                                      | (reserved)                                                                  |
| 25  |                                      | (reserved)                                                                  |
| 24  |                                      | (reserved)                                                                  |
| 23  |                                      | (reserved)                                                                  |
| 22  |                                      | (reserved)                                                                  |
| 21  |                                      | (reserved)                                                                  |
| 20  |                                      | (reserved)                                                                  |
| 19  |                                      | (reserved)                                                                  |
| 18  |                                      | (reserved)                                                                  |
| 17  |                                      | (reserved)                                                                  |
| 16  |                                      | (reserved)                                                                  |
| 15  |                                      | (reserved)                                                                  |
| 14  |                                      | (reserved)                                                                  |
| 13  |                                      | (reserved)                                                                  |
| 12  |                                      | (reserved)                                                                  |
| 11  |                                      | (reserved)                                                                  |
| 10  |                                      | (reserved)                                                                  |
| 9   | TWAIFD_CLK_EN                       | Configures whether to force enable the register configuration clock signal.<br>0: Disable<br>1: Enable (R/W) |
| 8   | TWAIFD_FORCE_RXBUF_MEM_CLK_ON       | Configures whether to force enable the RX buffer RAM clock signal.<br>0: Disable<br>1: Enable (R/W) |
```