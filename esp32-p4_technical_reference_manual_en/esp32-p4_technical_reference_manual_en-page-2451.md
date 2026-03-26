

```markdown
| Signal                  | Direction | Function                                                                 |
|-------------------------|-----------|---------------------------------------------------------------------------|
| I2SnI_BCK_in            | Input     | In I2Sn slave mode, inputs BCK signal for RX unit.                       |
| I2SnI_BCK_out           | Output    | In I2Sn master mode, outputs BCK signal for RX unit.                     |
| I2SnI_WS_in             | Input     | In I2Sn slave mode, inputs WS signal for RX unit.                        |
| I2SnI_WS_out            | Output    | In I2Sn master mode, outputs WS signal for RX unit.                      |
| I2SnI_Data_in           | Input     | Works as the serial input data bus for I2Sn RX unit.                     |
| I2SnO_Data_out          | Output    | Works as the serial output data bus for I2Sn TX unit.                    |
| I2SnO_BCK_in            | Input     | In I2Sn slave mode, inputs BCK signal for TX unit.                       |
| I2SnO_BCK_out           | Output    | In I2Sn master mode, outputs BCK signal for TX unit.                     |
| I2SnO_WS_in             | Input     | In I2Sn slave mode, inputs WS signal for TX unit.                        |
| I2SnO_WS_out            | Output    | In I2Sn master mode, outputs WS signal for TX unit.                      |
| I2Sn_MCLK_in            | Input     | In I2Sn slave mode, works as a clock source from the external master.    |
| I2Sn_MCLK_out           | Output    | In I2Sn master mode, works as a clock source for the external slave.     |
| I2SOI_Data1_in          | Input     | When the PDM-to-PCM converter is enabled, works as the serial input data line for RX unit. |
| I2SOI_Data2_in          | Input     | When the PDM-to-PCM converter is enabled, works as the serial input data line for RX unit. |
| I2SOI_Data3_in          | Input     | When the PDM-to-PCM converter is enabled, works as the serial input data line for RX unit. |
| I2SOO_Data1_out         | Output    | When the PCM-to-PDM converter is enabled, works as the serial output data line for TX unit. |

\* Any required signals of I2Sn must be mapped to the chip's pins via HP GPIO matrix, see Chapter 9 GPIO Matrix and IO MUX.
```

## 46.5 Supported Audio Standards

ESP32-P4 I2Sn supports multiple audio standards, including TDM Philips standard, TDM MSB alignment standard, TDM PCM standard, and PDM standard.

Select the needed standard by configuring the following bits:

*   **I2S_TX/RX_TDM_EN**
    - 0: Disable TDM mode
    - 1: Enable TDM mode

*   **I2S_TX/RX_PDM_EN**
    - 0: Disable PDM mode
    - 1: Enable PDM mode

*   **I2S_TX/RX_MSB_SHIFT**
    - 0: WS and SD signals change simultaneously, i.e., enable MSB alignment standard
```