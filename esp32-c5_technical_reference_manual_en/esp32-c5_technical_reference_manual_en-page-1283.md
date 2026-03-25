

```markdown
| Signal               | Direction | Function                                                                 |
|----------------------|-----------|---------------------------------------------------------------------------|
| I2SI_BCK_in          | Input     | In I2S slave mode, inputs BCK signal for RX unit.                        |
| I2SI_BCK_out         | Output    | In I2S master mode, outputs BCK signal for RX unit.                      |
| I2SI_WS_in           | Input     | In I2S slave mode, inputs WS signal for RX unit.                         |
| I2SI_WS_out          | Output    | In I2S master mode, outputs WS signal for RX unit.                       |
| I2SI_SD_in           | Input     | Works as the serial input data bus for I2S RX unit.                      |
| I2SO_SD_out          | Output    | Works as the serial output data bus for I2S TX unit.                     |
| I2SO_BCK_in          | Input     | In I2S slave mode, inputs BCK signal for TX unit.                        |
| I2SO_BCK_out         | Output    | In I2S master mode, outputs BCK signal for TX unit.                      |
| I2SO_WS_in           | Input     | In I2S slave mode, inputs WS signal for TX unit.                         |
| I2SO_WS_out          | Output    | In I2S master mode, outputs WS signal for TX unit.                       |
| I2S_MCLK_in          | Input     | In I2S slave mode, works as a clock source from the external master.     |
| I2S_MCLK_out         | Output    | In I2S master mode, works as a clock source for the external slave.      |
| I2SO_SD1_out         | Output    | When the PCM-to-PDM converter is enabled, works as the serial output data line for TX unit. |

\* Any required signals of I2S must be mapped to the chip's pins via GPIO matrix, see Chapter 8 GPIO Matrix and IO MUX.
```

## 35.5 Supported Audio Standards

ESP32-C5 I2S supports multiple audio standards, including TDM Philips standard, TDM MSB alignment standard, TDM PCM standard, and PDM standard.

Select the needed standard by configuring the following bits:

*   `I2S_TX/RX_TDM_EN`
    - 0: Disable TDM mode
    - 1: Enable TDM mode

*   `I2S_TX/RX_PDM_EN`
    - 0: Disable PDM mode
    - 1: Enable PDM mode

*   `I2S_TX/RX_MSB_SHIFT`
    - 0: WS and SD signals change simultaneously, i.e., enable MSB alignment standard
    - 1: WS signal changes one BCK clock cycle earlier than SD signal, i.e., enable Philips standard or select PCM standard

**Note:**  
`I2S_TX/RX_TDM_EN` and `I2S_TX/RX_PDM_EN` must not be configured to 1 or 0 at the same time, otherwise ESP32-C5 I2S will transmit data incorrectly in a mode that is neither TDM nor PDM.
```