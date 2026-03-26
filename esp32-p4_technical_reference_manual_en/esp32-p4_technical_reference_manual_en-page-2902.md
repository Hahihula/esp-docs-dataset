

```markdown
Register 57.4. RMT_CHmCONFO_REG (m: 4-7) (0x0030, 0x0038, 0x0040, 0x0048)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 30  | RMT_CARRIER_OUT_LV_CHm        | Configures the position of carrier wave for channel m.                      |
| 29  | RMT_CARRIER_EN_CHm            | Configures whether to enable carrier demodulation on output signal for channel m. |
| 28  | RMT_MEM_SIZE_CHm              | Configures the maximum number of memory blocks allocated to channel m.       |
| 27  | RMT_DMA_ACCESS_EN_CH7         | Configures whether to enable the DMA access function for channel 7. This field is reserved for channel 4 ~ 6. |
| 24  | RMT_IDLE_THRES_CHm            | Configures RX threshold. When no edge is detected on the input signal for continuous clock cycles longer than this field value, the receiver stops receiving data. Measurement unit: clk_div (R/W) |
| 23  | RMT_DIV_CNT_CHm               | Configures the clock divider of channel m. Measurement unit: rmt_sclk (R/W)   |
| 22  |                                |                                                                             |
|     | O: Disable                    |                                                                                 |
|     | 1: Enable                    |                                                                                 |
|     | (R/W)                       |                                                                                 |

RMT_DIV_CNT_CHm Configures the clock divider of channel m.
Measurement unit: rmt_sclk
(R/W)

RMT_IDLE_THRES_CHm Configures RX threshold. When no edge is detected on the input signal for continuous clock cycles longer than this field value, the receiver stops receiving data.
Measurement unit: clk_div
(R/W)

RMT_DMA_ACCESS_EN_CH7 Configures whether to enable the DMA access function for channel 7. This field is reserved for channel 4 ~ 6.
O: Disable
1: Enable
(R/W)

RMT_MEM_SIZE_CHm Configures the maximum number of memory blocks allocated to channel m.
(R/W)

RMT_CARRIER_EN_CHm Configures whether to enable carrier demodulation on output signal for channel m.
O: Disable
1: Enable
(R/W)

RMT_CARRIER_OUT_LV_CHm Configures the position of carrier wave for channel m.
O: Demodulate carrier wave on low level
1: Demodulate carrier wave on high level
(R/W)
```