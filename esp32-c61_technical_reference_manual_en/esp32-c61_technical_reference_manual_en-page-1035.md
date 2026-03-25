
```markdown
Note:
I2S_TX_TDM_EN and I2S_TX_PDM_EN must not be cleared or set simultaneously.

28.9.2.1 TDM TX Mode

In TDM TX mode, I2S supports up to 16 channels to transmit data. The total number of TX channels in use is controlled by I2S_TX_TDM_TOT_CHAN_NUM. For example, if I2S_TX_TDM_TOT_CHAN_NUM is set to 5, six channels in total (channel 0-5) will be used to transmit data. See Figure 28.9-2.

Note:
Most stereo I2S codecs can be controlled by setting the I2S module into 2-channel mode under TDM standard.

In these TX channels, if I2S_TX_TDM_CHANn_EN is set to:

• 1: This channel transmits the channel data out;
• 0: The TX data to be sent by this channel is controlled by I2S_TX_CHAN_EQUAL:
    – 1: The data of the previous channel is sent out;
    – 0: The data stored in I2S_SINGLE_DATA is sent out.

In TDM TX master mode, WS signal is controlled by I2S_TX_WS_IDLE_POL and I2S_TX_TDM_WS_WIDTH:

• I2S_TX_WS_IDLE_POL: The default level of WS signal;
• I2S_TX_TDM_WS_WIDTH: The cycles the WS default level lasts for when transmitting all channel data.
I2S_TX_HALF_SAMPLE_BITS x 2 is equal to the BCK cycles in one WS period.

TDM Channel Configuration Example

In this example, the register configuration is as follows:

• I2S_TX_TDM_CHAN_NUM = 5, i.e., channel 0-5 are used to transmit data.
• I2S_TX_CHAN_EQUAL = 1, i.e., data of the previous channel will be transmitted if the I2S_TX_TDM_CHANn_EN (n = 0-5) is cleared.
• I2S_TX_TDM_CHAN0/2/5_EN = 1, i.e., these channels transmit their channel data out.
• I2S_TX_TDM_CHAN1/3/4_EN = 0, i.e., these channels transmit the previous channel’s data out.

Once the configuration is done, data is transmitted as follows.

Figure 28.9-2. TDM Channel Control

I2S_TX_TDM_CHAN_NUM = 5; I2S_TX_CHAN_EQUAL = 1;
I2S_TX_TDM_CHAN0_EN = 1; I2S_TX_TDM_CHAN1_EN = 0; I2S_TX_TDM_CHAN2_EN = 1;
I2S_TX_TDM_CHAN3_EN = 0; I2S_TX_TDM_CHAN4_EN = 0; I2S_TX_TDM_CHAN5_EN = 1;
```