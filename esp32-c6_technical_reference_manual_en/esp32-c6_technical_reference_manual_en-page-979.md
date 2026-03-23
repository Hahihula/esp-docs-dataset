

```markdown
Chapter 30 I2S Controller (I2S)

Figure 30.5-2. TDM MSB Alignment Standard Timing Diagram


30.5.3 TDM PCM Standard

Short frame synchronization under PCM standard requires that WS signal changes one BCK clock cycle earlier than SD signal on the falling edge of BCK, which means that the WS signal becomes valid one clock cycle before transferring the first bit of channel data and remains unchanged in this BCK clock cycle. SD signal line transmits the most significant bit of audio data first.

Compared with PCM standard, TDM PCM standard supports multiple channels. See Figure 30.5-3.

Figure 30.5-3. TDM PCM Standard Timing Diagram


30.5.4 PDM Standard

Under PDM standard, WS signal changes continuously during data transmission. The low-level and high-level of this signal indicates the left channel and right channel respectively. WS and SD signals change simultaneously on the falling edge of BCK. See Figure 30.5-4.
```