

```markdown
- 1: WS signal changes one BCK clock cycle earlier than SD signal, i.e., enable Philips standard or select PCM standard

Note:
I2S_TX/RX_TDM_EN and I2S_TX/RX_PDM_EN must not be configured to 1 or 0 at the same time, otherwise ESP32-P4 I2Sn will transmit data incorrectly in a mode that is neither TDM nor PDM.
```

## 46.5.1 TDM Philips Standard

Philips specifications require that WS signal changes one BCK clock cycle earlier than SD signal on BCK falling edge, which means that WS signal is valid from one clock cycle before transmitting the first bit of channel data and changes one clock before the end of channel data transfer. SD signal line transmits the most significant bit of audio data first.

Compared with the Philips standard, TDM Philips standard supports multiple channels. See Figure 46.5-1.

Figure 46.5-1. TDM Philips Standard Timing Diagram

## 46.5.2 TDM MSB Alignment Standard

MSB alignment specifications require that WS and SD signals change simultaneously on the falling edge of BCK. The WS signal is valid until the end of the channel data transfer. The SD signal line transmits the most significant bit of audio data first.

Compared with MSB alignment standard, TDM MSB alignment standard supports multiple channels. See Figure 46.5-2.
```