

```markdown
- 0: disable PDM mode.
- 1: enable PDM mode.

* I2S_TX/RX_MSB_SHIFT
    - 0: WS and SD signals change simultaneously, i.e. enable MSB alignment standard.
    - 1: WS signal changes one BCK clock cycle earlier than SD signal, i.e. enable Philips standard or select PCM standard.

* I2S_TX/RX_PCM_BYPASS
    - 0: enable PCM standard.
    - 1: disable PCM standard.


### 29.5.1 TDM Philips Standard

Philips specifications require that WS signal changes one BCK clock cycle earlier than SD signal on BCK falling edge, which means that WS signal is valid from one clock cycle before transmitting the first bit of channel data and changes one clock before the end of channel data transfer. SD signal line transmits the most significant bit of audio data first.

Compared with Philips standard, TDM Philips standard supports multiple channels, see Figure 29.5-1.



![Figure 29.5-1. TDM Philips Standard Timing Diagram](image)

### 29.5.2 TDM MSB Alignment Standard

MSB alignment specifications require WS and SD signals change simultaneously on the falling edge of BCK. The WS signal is valid until the end of channel data transfer. The SD signal line transmits the most significant bit of audio data first.

Compared with MSB alignment standard, TDM MSB alignment standard supports multiple channels, see Figure 29.5-2.
```