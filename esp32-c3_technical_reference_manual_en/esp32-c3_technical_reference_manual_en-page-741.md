

```markdown
Chapter 29 I2S Controller (I2S)
GoBack

At this point, the first phase of data format control is complete.

29.9.1.4 Bit Width Control of Channel TX Data

The TX data width in each channel is determined by `I2S_TX_TDM_CHAN_BITS`.

- If TX data width in each channel is larger than the valid data width, zeros will be filled to these extra bits.
  Configure `I2S_TX_LEFT_ALIGN` to:
    - 0: the valid data is at the lower bits of TX data. Zeros are filled into higher bits of TX data.
    - 1: the valid data is at the higher bits of TX data. Zeros are filled into lower bits of TX data.

- If the TX data width in each channel is smaller than the valid data width, only the lower bits of valid data are sent out, and the higher bits are discarded.

At this point, the second phase of data format control is complete.

29.9.1.5 Bit Order Control of Channel Data

The data bit order in each channel is controlled by `I2S_TX_BIT_ORDER`:

- 0: Not reverse the valid data bit order;
- 1: Reverse the valid data bit order.

At this point, the data format control is complete. Figure 29.9-1 shows a complete process of TX data format control.

Figure 29.9-1. TX Data Format Control
```