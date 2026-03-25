

```markdown
Register 42.3. RMT_CHmCONFO_REG (m: 2-3) (0x0018+0x8*(m-2))

Continued from the previous page...

RMT_MEM_SIZE_CHm Configures the maximum number of memory blocks allocated to channel m.
(R/W)

RMT_CARRIER_EN_CHm Configures whether to enable carrier modulation on output signal for
channel m.
O: Disable
1: Enable
(R/W)

RMT_CARRIER_OUT_LV_CHm Configures the position of carrier wave for channel m.
O: Add carrier wave on low level
1: Add carrier wave on high level
(R/W)


Register 42.4. RMT_CHmCONF1_REG (m: 2-3) (0x001C+0x8*(m-2))

| 31 | 16 | 15 | 14 | 13 | 12 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|----:|----:|----:|---:|---:|---:|---:|---:|---:|
|    0|    0|    0|    0|    0|    0|   0|   1|   0|   0|   0| Reset |
| (reserved) | RMT_CONF_UPDATE_CHm | (reserved) | RMT_MEM_RX_WRAP_EN_CHm | RMT_RX_FILTER_THRES_CHm | RMT_RX_FILTER_EN_CHm | RMT_MEM_OWNER_CHm | RMT_APB_MEM_WR_RST_CHm | RMT_RX_EN_CHm |

RMT_RX_EN_CHm Configures whether to enable the receiver to start receiving data in channel m.
O: Disable
1: Enable
(R/W)

RMT_MEM_WR_RST_CHm Configures whether to reset RAM write address accessed by the re-
ceiver for channel m.
O: No effect
1: Reset
(WT)

RMT_APB_MEM_RST_CHm Configures whether to reset RAM W/R address accessed by APB FIFO
for channel m.
O: No effect
1: Reset
(WT)

Continued on the next page...
```