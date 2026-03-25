

```markdown
Chapter 28 I2S Controller (I2S) GoBack

Figure 28.5-1. TDM Philips Standard Timing Diagram

28.5.2 TDM MSB Alignment Standard

MSB alignment standards require that WS and SD signals change simultaneously on the falling edge of BCK.
The WS signal is valid until the end of the channel data transfer. The SD signal line transmits the most
significant bit of audio data first.

Compared with the basic MSB alignment standard, TDM MSB alignment standard supports multiple channels.

See Figure 28.5-2.

Figure 28.5-2. TDM MSB Alignment Standard Timing Diagram

28.5.3 TDM PCM Standard

Short frame synchronization under the PCM standards requires that the WS signal changes one BCK clock
cycle earlier than the SD signal on the falling edge of BCK, which means that the WS signal becomes valid one
clock cycle before transferring the first bit of channel data and remains unchanged in this BCK clock cycle. SD
signal line first transmits the most significant bit of audio data.

Compared with the basic PCM standard, TDM PCM standard supports multiple channels. See Figure 28.5-3.
```