

```markdown
Register 47.7. LP_I2S_INT_RAW_REG (0x000C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_I2S_RX_DONE_INT_RAW                     | The raw interrupt status of the `LP_I2S_RX_DONE_INT` interrupt.             |
|     | `(R/SS/WTC)`                               |                                                                             |
| 29  | LP_I2S_RX_HUNG_INT_RAW                     | The raw interrupt status of the `LP_I2S_RX_DONE_INT` interrupt.            |
|     | `(R/SS/WTC)`                               |                                                                             |
| 28  | LP_I2S_RX_FIFOMEM_UFD_INT_RAW              | The raw interrupt status of the `LP_I2S_RX_FIFOMEM_UFD_INT` interrupt.      |
|     | `(R/SS/WTC)`                               |                                                                             |
| 27  | LP_I2S_VAD_DONE_INT_RAW                    | The raw interrupt status of the `LP_I2S_VAD_DONE_INT` interrupt.           |
|     | `(R/SS/WTC)`                               |                                                                             |
| 26  | LP_I2S_VAD_RESET_DONE_INT_RAW              | The raw interrupt status of the `LP_I2S_VAD_RESET_DONE_INT` interrupt.     |
|     | `(R/SS/WTC)`                               |                                                                             |
| 25  | LP_I2S_RX_MEM_THRESHOLD_INT_RAW            | The raw interrupt status of the `LP_I2S_RX_MEM_THRESHOLD_INT` interrupt.   |
|     | `(R/SS/WTC)`                               |                                                                             |

```