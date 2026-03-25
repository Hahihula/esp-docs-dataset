

```markdown
| Signal          | Direction | Function                                                                                                                                              |
|-----------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| I2SI_BCK_in     | Input     | In I2S slave mode, inputs BCK signal for RX unit.                                                                                                        |
| I2SI_BCK_out    | Output     | In I2S master mode, outputs BCK signal for RX unit.                                                                                                      |
| I2SI_WS_in      | Input     | In I2S slave mode, inputs WS signal for RX unit.                                                                                                         |
| I2SI_WS_out     | Output     | In I2S master mode, outputs WS signal for RX unit.                                                                                                       |
| I2SI_SD_in      | Input     | Works as the serial input data bus for I2S RX unit.                                                                                                      |
| I2SO_SD_out     | Output     | Works as the serial output data bus for I2S TX unit.                                                                                                     |
| I2SO_BCK_in     | Input     | In I2S slave mode, inputs BCK signal for TX unit.                                                                                                        |
| I2SO_BCK_out    | Output     | In I2S master mode, outputs BCK signal for TX unit.                                                                                                      |
| I2SO_WS_in      | Input     | In I2S slave mode, inputs WS signal for TX unit.                                                                                                         |
| I2SO_WS_out     | Output     | In I2S master mode, outputs WS signal for TX unit.                                                                                                       |
| I2S_MCLK_in     | Input     | In I2S slave mode, works as a clock source from the external master.                                                                                    |
| I2S_MCLK_out    | Output     | In I2S master mode, works as a clock source for the external slave.                                                                                      |
| I2SO_SD1_out    | Output     | When the PCM-to-PDM converter is enabled, works as the serial output data line for TX unit.                                                              |

* Any required signals of I2S must be mapped to the chip’s pins via GPIO matrix. See Chapter 6 GPIO Matrix and IO MUX.
```