

```markdown
Register 37.4. RMT_CHmCONF1_REG (m: 2-3) (0x0000C+0x8*m)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 16  | RMT_CONF_UPDATE_CHm                                                         |
| 15  | (reserved)                                                                  |
| 14  | RMT_MEM_RX_WRAP_EN_CHm                                                      |
| 13  | RMT_RX_FILTER_THRES_CHm                                                     |
| 12  | RMT_RX_FILTER_EN_CHm                                                        |
| 11  | RMT_RX_APP_MEM_OWN_CHm                                                      |
| 10  | RMT_RX_WR_RST_CHm                                                            |
| 9   | RMT_RX_EN_CHm                                                                |
| 8   | Oxf                                                                        |
| 7   | 0                                                                            |
| 6   | 1                                                                            |
| 5   | 0                                                                            |
| 4   | Reset                                                                       |

RMT_RX_EN_CHm Configures whether to enable the receiver to start receiving data in channel m.
O: Disable
1: Enable
(R/W)

RMT_MEM_WR_RST_CHm Configures whether to reset RAM write address accessed by the receiver for channel m.
O: No effect
1: Reset
(WT)

RMT_APB_MEM_RST_CHm Configures whether to reset RAM W/R address accessed by APB FIFO for channel m.
O: No effect
1: Reset
(WT)

RMT_MEM_OWNER_CHm Configures the ownership of channel m's RAM block.
O: APB bus is using the RAM
1: Receiver is using the RAM
(R/W/SC)

RMT_RX_FILTER_EN_CHm Configures whether to enable the receiver's filter for channel m.
O: Disable
1: Enable
(R/W)

RMT_RX_FILTER_THRES_CHm Configures whether the receiver, when receiving data, ignores the input pulse when its width is shorter than this register value in units of rmt_sclk cycles.
O: No effect
1: Reset
(R/W)

RMT_MEM_RX_WRAP_EN_CHm Configures whether to enable wrap RX mode for channel m.
O: Disable
1: Enable
In this mode, if the RX data size is larger than channel m's RAM block size, the receiver stores the RX data from the first address to the last address in loops.
(R/W)

RMT_CONF_UPDATE_CHm Synchronization bit for channel m. (WT)
```