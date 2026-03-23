

```markdown
Chapter 30 I2S Controller (I2S)

In these TX channels, if `I2S_TX_TDM_CHANn_EN` is set to:
*   1: this channel sends the channel data out;
*   0: the TX data to be sent by this channel is controlled by `I2S_TX_CHAN_EQUAL`:
    *   - 1: the data of previous channel is sent out;
    *   - 0: the data stored in `I2S_SINGLE_DATA` is sent out.

In TDM TX master mode, WS signal is controlled by `I2S_TX_WS_IDLE_POL` and
`I2S_TX_TDM_WS_WIDTH`:
*   `I2S_TX_WS_IDLE_POL`: the default level of WS signal;
*   `I2S_TX_TDM_WS_WIDTH`: the cycles the WS default level lasts for when transmitting all channel data.
    `I2S_TX_HALF_SAMPLE_BITS x 2` is equal to the BCK cycles in one WS period.

TDM Channel Configuration Example

In this example, register configuration is as follows:
*   `I2S_TX_TDM_CHAN_NUM = 5`, i.e., channel 0 ~ 5 are used to transmit data.
*   `I2S_TX_CHAN_EQUAL = 1`, i.e., that data of previous channel will be transmitted if the bit
    `I2S_TX_TDM_CHANn_EN` is cleared. n = 0 ~ 5.
*   `I2S_TX_TDM_CHANO/2/5_EN = 1`, i.e., these channels send their channel data out.
*   `I2S_TX_TDM_CHAN1/3/4_EN = 0`, i.e., these channels send the previous channel data out.

Once the configuration is done, data is transmitted as follows:

![Figure 30.9-2. TDM Channel Control](image)

```
```markdown
I2S_TX_TDM_CHAN_NUM = 5; I2S_TX_CHAN_EQUAL = 1;
I2S_TX_TDM_CHANO_EN = 1; I2S_TX_TDM_CHAN1_EN = 0; I2S_TX_TDM_CHAN2_EN = 1;
I2S_TX_TDM_CHAN3_EN = 0; I2S_TX_TDM_CHAN4_EN = 0; I2S_TX_TDM_CHAN5_EN = 1;

Figure 30.9-2. TDM Channel Control
```

### 30.9.2.2 I2S Channel Control in PDM TX Mode

ESP32-C6 I2S supports two PDM TX modes, namely, normal PDM TX mode and PCM-to-PDM TX mode.

In PDM TX mode, fetching data through DMA is controlled by `I2S_TX_MONO` and `I2S_TX_MONO_FST_VLD`.
See Table 30.9-4. Please configure the two bits according to the data stored in memory, be it the
single-channel or dual-channel data.
```