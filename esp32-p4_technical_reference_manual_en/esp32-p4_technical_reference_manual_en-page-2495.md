

```markdown
- WS
- SD

• “C” represents the signal direction, which includes:
    – “in”: Input signal into the LP I2S module
    – “out”: Output signal from the LP I2S module

Table 47.3-1 provides a detailed description of LP I2S signals.

Table 47.3-1. LP I2S Signal Description

| Signal* | Direction | Function |
|---------|-----------|----------|
| LP_I2SI_BCK_in | Input | In LP I2S slave mode, inputs BCK signal for RX unit |
| LP_I2SI_BCK_out | Output | In LP I2S master mode, outputs BCK signal for RX unit |
| LP_I2SI_WS_in | Input | In LP I2S slave mode, inputs WS signal for RX unit |
| LP_I2SI_WS_out | Output | In LP I2S master mode, outputs WS signal for RX unit |
| LP_I2SI_SD_in | Input | Serial input data bus for LP I2S RX unit |
| LP_I2S_MCLK_out | Output | LP I2S master clock output |

* Any required signals of LP I2S must be mapped to the chip’s pins via LP GPIO matrix. See Chapter 9 GPIO Matrix and IO MUX.

47.4 Supported Audio Standards

ESP32-P4 I2S supports multiple audio standards, including TDM Philips standard, TDM MSB alignment standard, TDM PCM standard, and PDM standard.

Select the needed standard by configuring the following bits:

• LP_I2S_RX_TDM_EN
    – 0: Disable TDM mode
    – 1: Enable TDM mode

• LP_I2S_RX_PDM_EN
    – 0: Disable PDM mode
    – 1: Enable PDM mode

• LP_I2S_RX_MSB_SHIFT
    – 0: WS and SD signals change simultaneously, i.e., enable MSB alignment standard
    – 1: WS signal changes one BCK clock cycle earlier than SD signal, i.e., enable Philips standard or select PCM standard

Note:
LP_I2S_RX_TDM_EN and LP_I2S_RX_PDM_EN must not be configured to 1 or 0 at the same time, otherwise LP I2S will transmit data incorrectly in a mode that is neither TDM nor PDM.
```