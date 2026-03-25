

```markdown
Chapter 31 I2S Controller (I2S) GoBack


### 31.9.1.4 Bit Width Control of Channel TX Data

The TX data width in each channel is determined by `I2S_TX_TDM_CHAN_BITS`.

* If TX data width in each channel is larger than the valid data width, zeros will be filled to these extra bits. Configure `I2S_TX_LEFT_ALIGN`:
    - 0: The valid data is at the lower bits of TX data. Zeros are filled into higher bits of TX data;
    - 1: The valid data is at the higher bits of TX data. Zeros are filled into lower bits of TX data.
* If the TX data width in each channel is smaller than the valid data width, only the lower bits of valid data are sent out, and the higher bits are discarded.

At this point, the second phase of data format control is completed.


### 31.9.1.5 Bit Order Control of Channel Data

The data bit order in each channel is controlled by `I2S_TX_BIT_ORDER`:

* 0: Not reverse the valid data bit order;
* 1: Reverse the valid data bit order.

At this point, the data format control is completed. The data after format control will be sent sequentially from high to low. Figure 31.9-1 shows the complete process of TX data format control.


I2S_TX_BITS_MOD = 23

```
| B2[7:0] | B1[7:0] | B0[7:0] |
```

I2S_TX_BIG_ENDIAN = 1

```
| B0[7:0] | B1[7:0] | B2[7:0] |
```

I2S_TX_TDM_CHAN_BITS = 31
I2S_TX_LEFT_ALIGN = 1

```
| B0[7:0] | B1[7:0] | B2[7:0] | 8'd0 |
```

I2S_TX_BIT_ORDER = 1

```
| B2[0:7] | B1[0:7] | B0[0:7] | 8'd0 |
```


Figure 31.9-1. TX Data Format Control


### 31.9.2 Channel Mode Control

ESP32-H2 I2S supports both TDM TX mode and PDM TX mode. Set `I2S_TX_TDM_EN` to enable TDM TX mode, or set `I2S_TX_PDM_EN` to enable PDM TX mode.
```