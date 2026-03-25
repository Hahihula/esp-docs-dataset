

```markdown
## 28.5 Supported Audio Standards

ESP32-C61 I2S supports multiple audio standards, including TDM Philips standard, TDM MSB alignment standard, TDM PCM standard, and PDM standard.

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
`I2S_TX/RX_TDM_EN` and `I2S_TX/RX_PDM_EN` must not be configured to 1 or 0 at the same time, otherwise ESP32-C61 I2S will transmit data incorrectly in a mode that is neither TDM nor PDM.

### 28.5.1 TDM Philips Standard

Philips standards require that WS signal changes one BCK clock cycle earlier than SD signal on BCK falling edge, which means that WS signal is valid from one clock cycle before transmitting the first bit of channel data and changes one clock before the end of channel data transfer. SD signal line transmits the most significant bit of audio data first.

Compared with the basic Philips standard, TDM Philips standard supports multiple channels. See Figure 28.5-1.
```