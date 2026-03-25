

```markdown
Register 43.7. PARL_IO_TX_GENRL_CFG_REG (0x0018)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
| 30  | PARL_IO_TX_VALID_OUTPUT_EN     | Configures whether to select DMA output data or the chip select signal (CS) as the control source of TXD MSB. <br> 0: Select the DMA output data as the control source<br> 1: Select the chip select signal (CS) as the control source<br>(R/W) |
| 29  | PARL_IO_TX_GATING_EN           | Configures whether to enable the clock gating of the TX output clock. <br> 0: Disable<br> 1: Enable<br>(R/W) |
| 14  | PARL_IO_TX_IDLE_VALUE          | Configures the data value on TX bus in idle state. (R/W)                     |
| 13  |                                 |                                                                             |
| 12  | PARL_IO_TX_EOF_GEN_SEL         | Configures the generation mechanism of TX EOF. <br> 0: Generate TX EOF by the configured data bit length<br> 1: Generate TX EOF by the GDMA EOF signal.<br>(R/W) |

Register 43.8. PARL_IO_FIFO_CFG_REG (0x001C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
| 30  | PARL_IO_TX_FIFO_SRST           | Configures whether to reset async FIFO in the TX unit. <br> 0: No effect<br> 1: Reset<br>(R/W) |
| 29  | PARL_IO_RX_FIFO_SRST           | Configures whether to reset async FIFO in the RX unit. <br> 0: No effect<br> 1: Reset<br>(R/W) |
```