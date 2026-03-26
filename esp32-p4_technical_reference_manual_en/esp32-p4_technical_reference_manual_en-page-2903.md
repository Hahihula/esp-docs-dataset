

```markdown
Register 57.5. RMT_CHmCONF1_REG (m: 4-7) (0x0034, 0x003C, 0x0044, 0x004C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 16  | RMT_CONF_UPDATE_CHm           | Synchronization bit for channel m. (WT)                                     |
| 15  | (reserved)                    |                                                                             |
| 14  | RMT_MEM_RX_WRAP_EN_CHm        | Configures whether to enable wrap RX mode for channel m.                    |
| 13  | RMT_RX_FILTER_THRES_CHm       | Configures the receiver, when receiving data, ignores the input pulse when its width is shorter than this register value in units of rmt_sclk cycles. O: No effect<br>1: Reset (R/W) |
| 12  | RMT_RX_FILTER_EN_CHm          | Configures whether to enable the receiver’s filter for channel m.<br>O: Disable<br>1: Enable (R/W) |
| 11  | RMT_MEM_OWNER_CHm             | Configures the ownership of channel m’s RAM block.<br>O: APB bus is using the RAM<br>1: Receiver is using the RAM (R/W/SC) |
| 10  | RMT_APB_MEM_RST_CHm           | Configures whether to reset RAM W/R address accessed by APB FIFO for channel m.<br>O: No effect<br>1: Reset (WT) |
| 9   | RMT_MEM_WR_RST_CHm            | Configures whether to reset RAM write address accessed by the receiver for channel m.<br>O: No effect<br>1: Reset (WT) |
| 8   | RMT_RX_EN_CHm                 | Configures whether to enable the receiver to start receiving data in channel m.<br>O: Disable<br>1: Enable (R/W) |
```