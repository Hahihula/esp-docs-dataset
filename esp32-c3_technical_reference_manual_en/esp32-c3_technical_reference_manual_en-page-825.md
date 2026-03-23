

```markdown
Register 31.26. TWAI_INT_RAW_REG (0x000C)

| Bit | Name                                 | Description                                                                                                                                                                                                 |
|-----|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31  |                                       | (reserved)                                                                                                                                                                                                |
| 9   | TWAI_BUS_STATE_INT_ST                | Bus state interrupt. If this bit is set to 1, it indicates the status of TWAI controller has changed. (RO)<br>                                                                                              |
| 8   | TWAI_ERR_WARN_INT_ST                 | Error warning interrupt. If this bit is set to 1, it indicates the error status signal and the bus-off status signal of Status register have changed (e.g., switched from 0 to 1 or from 1 to 0). (RO)<br>                                                                    |
| 7   | TWAI_OVERRUN_INT_ST                  | Data overrun interrupt. If this bit is set to 1, it indicates a data overrun interrupt is generated in the RX FIFO. (RO)<br>                                                                                   |
| 6   | TWAI_ERR_PASSIVE_INT_ST              | Error passive interrupt. If this bit is set to 1, it indicates the TWAI Controller is switched between error active status and error passive status due to the change of error counters. (RO)<br>                                                                             |
| 5   | TWAI_ARB_LOST_INT_ST                 | Arbitration lost interrupt. If this bit is set to 1, it indicates an arbitration lost interrupt is generated. (RO)<br>                                                                                       |
| 4   | TWAI_BUS_ERR_INT_ST                  | Error interrupt. If this bit is set to 1, it indicates an error is detected on the bus. (RO)<br>                                                                                                             |
| 3   | TWAI_TX_RX_INT_ST                    | Transmit interrupt. If this bit is set to 1, it indicates the message transmission is finished and a new transmission is able to start. (RO)<br><br>                                                         |
| 2   | TWAI_RX_INT_ST                       | Receive interrupt. If this bit is set to 1, it indicates there are messages to be handled in the RX FIFO. (RO)<br><br>                                                                                         |
```