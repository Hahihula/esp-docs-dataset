

```markdown
Register 33.4. RMT_CHmCONFO_REG (m = 2, 3) (0x0018, 0x0020)

| (reserved) | RMT_CARRIER_OUT_LV_CHm | RMT_CARRIER_EN_CHm | (reserved) | RMT_MEM_SIZE_CHm | RMT_IDLE_THRES_CHm |
|:-----------:|:----------------------:|:------------------:|:-----------:|:-----------------:|:-------------------:|
|     31      |         30             |        29         |     28      |         27        |          26         |
|             |                        |                    |             |                   |                     |
|    0        |           1            |         0          |     0x1     |       0x7fff      |        0x2          |
|             |                        |                    |             |                   |                     |

RMT_DIV_CNT_CHm This field is used to configure the clock divider of channel m. (R/W)

RMT_IDLE_THRES_CHm This field is used to configure RX threshold. When no edge is detected on the input signal for continuous clock cycles longer than this field value, the receiver stops receiving data. (R/W)

RMT_MEM_SIZE_CHm This field is used to configure the maximum number of memory blocks allocated to channel m. (R/W)

RMT_CARRIER_EN_CHm This is the carrier modulation enable-bit for channel m. 1: Add carrier modulation on output signal. 0: No carrier modulation is added on output signal. (R/W)

RMT_CARRIER_OUT_LV_CHm This bit is used to configure the position of carrier wave for channel m. (R/W)
    1'h0: add carrier wave on low level.
    1'h1: add carrier wave on high level.
```