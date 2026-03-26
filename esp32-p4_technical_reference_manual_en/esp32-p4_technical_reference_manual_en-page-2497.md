

```markdown
## 47.4.3 TDM PCM Standard

Short frame synchronization under the PCM standards requires that the WS signal changes one BCK clock cycle earlier than the SD signal on the falling edge of BCK, which means that the WS signal becomes valid one clock cycle before transferring the first bit of channel data and remains unchanged in this BCK clock cycle. SD signal line first transmits the most significant bit of audio data.

Compared with the basic PCM standard, TDM PCM standard supports multiple channels. See Figure 47.4-3.

Figure 47.4-3. TDM PCM Standard Timing Diagram

## 47.4.4 PDM Standard

Under PDM standard, WS signal changes continuously during data transmission. The low-level and high-level of this signal indicates the left channel and right channel respectively. WS and SD signals change simultaneously on the falling edge of BCK. See Figure 47.4-4.

Figure 47.4-4. PDM Standard Timing Diagram

## 47.5 RX Clock

LP_I2S_RX_CLK is the master clock of LP I2S RX unit, divided from:
```