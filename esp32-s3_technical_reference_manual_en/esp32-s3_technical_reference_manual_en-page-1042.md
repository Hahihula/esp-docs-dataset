**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Table Header:**
Table 28.4-1. I2S Signal Description

| Signal* | Direction | Function |
|---------|-----------|----------|
| I2Sn!_BCK_in | Input | In slave mode, inputs BCK signal for RX unit. |
| I2Sn!_BCK_out | Output | In master mode, outputs BCK signal for RX unit. |
| I2Sn!_WS_in | Input | In slave mode, inputs WS signal for RX unit. |
| I2Sn!_WS_out | Output | In master mode, outputs WS signal for RX unit. |
| I2Sn!_Data_in | Input | Works as the serial input data bus for RX unit. |
| I2SnO_Data_out | Output | Works as the serial output data bus for TX unit. |
| I2SnO_BCK_in | Input | In slave mode, inputs BCK signal for TX unit. |
| I2SnO_BCK_out | Output | In master mode, outputs BCK signal for TX unit. |
| I2SnO_WS_in | Input | In slave mode, inputs WS signal for TX unit. |
| I2SnO_WS_out | Output | In master mode, outputs WS signal for TX unit. |
| I2Sn!_MCLK_in | Input | In slave mode, works as a clock source from the external master. |
| I2S!_MCLK_out | Output | In master mode, works as a clock source for the external slave. |
| I2SOI_Data1_in | Input | In PDM-to-PCM RX mode, works as the serial input data line for RX unit. |
| I2SOI_Data2_in | Input | In PDM-to-PCM RX mode, works as the serial input data line for RX unit. |
| I2SOI_Data3_in | Input | In PDM-to-PCM RX mode, works as the serial input data line for RX unit. |
| I2S0O_Data1_out | Output | In PCM-to-PDM TX mode, works as the serial output data line for TX unit. |

**Note:**
* Any required signals of I2Sn must be mapped to the chip's pins via GPIO matrix, see Chapter 6 IO MUX and GPIO Matrix (GPIO, IOMUX).

**Subsection Title:**
28.5 Supported Audio Standards

**Body Text:**
ESP32-S3 I2Sn supports multiple audio standards, including TDM Philips standard, TDM MSB alignment standard, TDM PCM standard, and PDM standard.

Select the standard by configuring the following bits:

- **I2S_TX/RX_TDM_EN**
  - `0`: disable TDM mode.
  - `1`: enable TDM mode. 

- **I2S_TX/RX_PDM_EN**
  - `0`: disable PDM mode.
  - `1`: enable PDM mode.

- **I2S_TX/RX_MSB_SHIFT**
  - `0`: WS and SD signals change simultaneously, i.e., enable MSB alignment standard. 
  - `1`: WS signal changes one BCK clock cycle earlier than SD signal, i.e., enable Philips standard or select PCM standard.

- **I2S_TX/RX_PCM_BYPASS**
  - `0`: enable PCM standard.
  - `1`: disable PCM standard.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback