**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Heading and Subsection with Content:**

**28.9.1.5 Bit Order Control of Channel Data**

The channel data will be stored as the data to be input in order from high to low. The data bit order in each channel is controlled by `I2S_TX_BIT_ORDER`:

- 0: Not reverse the valid data bit order;
- 1: Reverse the valid data bit order.

At this point, the data format control is complete. The data after format control will be sent sequentially from high to low. Figure [28.9-1](#) shows a complete process of TX data format control.
- `I2S_TX_BIT_SMOD = 23`
- `I2S_TX_BIG_ENDIAN = 1`

**Figure Caption:**
Figure 28.9-1. TX Data Format Control

**Diagram Description in Figure [28.9-1](#):**

```
B0[7:0] B1[7:0] B0[7:0]
I2S_TX_BIT_SMOD = 23
I2S_TX_BIG_ENDIAN = 1
```

**Section Heading and Subsection with Content:**

**28.9.2 Channel Mode Control**

ESP32-S3 I2S supports both TDM TX mode and PDM TX mode. Set `I2S_TX_TDM_EN` to enable TDM TX mode, or set `I2S_TX_PDM_EN` to enable PDM TX mode.

**Note:**
- `I2S_TX_TDM_EN` and `I2S_TX_PDM_EN` must not be cleared or set simultaneously.
- Most stereo I2S codecs can control the TDM module into 2-channel mode under standard settings of setting the `I2Sn` module to channel.

**Section Heading:**

**28.9.2.1 I2Sn Channel Control in TDM Mode**

In TDM mode, I2Sn supports up to 16 channels to output data. The total number of TX channels is controlled by `I2S_TX_TDMTot_CHAN_NUM`. For example, if `I2S_TX_TDMTot_CHAN_NUM` is set to 5, six channels in total (channel O ~ 5) will be used to transmit data.

In these TX channels, if `I2S_TX_TDMCHANEN` is set:

**Figure Caption:**
Figure [28.9-2](#)

**Footer Information:**

ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

---

*Note: The actual image of Figure 28.9-1 and the referenced figure for `I2S_TX_TDMTot_CHAN_NUM` are not provided in this text, so their contents cannot be described.*