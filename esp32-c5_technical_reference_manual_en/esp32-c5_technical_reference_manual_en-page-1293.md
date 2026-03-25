

```markdown
I2S_TX_HALF_SAMPLE_BITS x 2 is equal to the BCK cycles in one WS period.

TDM Channel Configuration Example

In this example, the register configuration is as follows:

*   I2S_TX_TDM_CHAN_NUM = 5, i.e., channel O-5 are used to transmit data.
*   I2S_TX_CHAN_EQUAL = 1, i.e., data of the previous channel will be transmitted if the I2S_TX_TDM_CHANn_EN (n = 0-5) is cleared.
*   I2S_TX_TDM_CHANO/2/5_EN = 1, i.e., these channels transmit their channel data out.
*   I2S_TX_TDM_CHAN1/3/4_EN = 0, i.e., these channels transmit the previous channel’s data out.

Once the configuration is done, data is transmitted as follows.

I2S_TX_TDM_CHAN_NUM = 5; I2S_TX_CHAN_EQUAL = 1;
I2S_TX_TDM_CHANO_EN = 1; I2S_TX_TDM_CHAN1_EN = 0; I2S_TX_TDM_CHAN2_EN = 1;
I2S_TX_TDM_CHAN3_EN = 0; I2S_TX_TDM_CHAN4_EN = 0; I2S_TX_TDM_CHAN5_EN = 1;

Figure 35.9-2. TDM Channel Control

35.9.2.2 PDM TX Mode

In PDM TX mode, I2S supports both PDM raw data transmission and PCM-to-PDM data format conversion.

In PDM TX mode, fetching data through GDMA is controlled by I2S_TX_MONO and I2S_TX_MONO_FST_VLD. See Table 35.9-3. Configure the two bits according to the data stored in memory, be it the single-channel or dual-channel data.

Table 35.9-3. Data-Fetching Control in PDM Mode

| Data-Fetching Control Option | Mode     | I2S_TX_MONO | I2S_TX_MONO_FST_VLD |
|------------------------------|----------|-------------|---------------------|
| Post data-fetching request to GDMA at any edge of WS signal               | Stereo mode | 0           | x                   |
| Post data-fetching request to GDMA only at the second half period of WS signal | Mono mode   | 1           | 0                   |
| Post data-fetching request to GDMA only at the first half period of WS signal | Mono mode   | 1           | 1                   |

When I2S is in PDM TX master mode, the default level of WS signal is controlled by I2S_TX_WS_IDLE_POL, and the WS signal frequency is half of the BCK signal frequency. The configuration of WS signal is similar to that of BCK signal. Please refer to Section 35.6 and Figure 35.6.

When transmitting raw PDM data, the I2S channel mode is controlled by I2S_TX_CHAN_MOD and I2S_TX_WS_IDLE_POL. See the table below.
```