

```markdown
Register 33.5. RMT_CHmCONF1_REG(m = 2, 3) (0x001C, 0x0024)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 31  |                                                                             |
| 16  | RMT_CONF_UPDATE_CHm Synchronization bit for channel m. (WT)                  |
| 15  | (reserved)                                                                  |
| 14  | RMT_MEM_RX_WRAP_EN_CHm Set this bit to enable wrap RX mode for channel m. In this mode, if the RX data size is larger than channel m's RAM block size, the receiver stores the RX data from the first address to the last address in loops. (R/W) |
| 13  | RMT_RX_FILTER_THRES_CHm When receiving data, the receiver ignores the input pulse when its width is shorter than this register value in units of rmt_sclk cycles. (R/W) |
| 12  | RMT_RX_FILTER_EN_CHm Set this bit to enable the receiver's filter for channel m. (R/W) |
| 11  | RMT_MEM_OWNER_CHm This bit marks the ownership of channel m's RAM block. (R/W/SC)<br>1'h1: Receiver is using the RAM.<br>1'h0: APB bus is using the RAM. |
| 10  | RMT_APB_MEM_RST_CHm Set this bit to reset RAM W/R address accessed by APB FIFO for channel m. (WT) |
| 9   | RMT_MEM_WR_RST_CHm Set this bit to reset RAM write address accessed by the receiver for channel m. (WT) |
| 8   | RMT_RX_EN_CHm Set this bit to enable the receiver to start receiving data in channel m. (R/W) |

```
```markdown
- RMT_RX_EN_CHm: Set this bit to enable the receiver to start receiving data in channel m. (R/W)
- RMT_MEM_WR_RST_CHm: Set this bit to reset RAM write address accessed by the receiver for channel m. (WT)
- RMT_APB_MEM_RST_CHm: Set this bit to reset RAM W/R address accessed by APB FIFO for channel m. (WT)
- RMT_MEM_OWNER_CHm: This bit marks the ownership of channel m's RAM block. (R/W/SC)<br>1'h1: Receiver is using the RAM.<br>1'h0: APB bus is using the RAM.
- RMT_RX_FILTER_EN_CHm: Set this bit to enable the receiver's filter for channel m. (R/W)
- RMT_RX_FILTER_THRES_CHm: When receiving data, the receiver ignores the input pulse when its width is shorter than this register value in units of rmt_sclk cycles. (R/W)
- RMT_MEM_RX_WRAP_EN_CHm: Set this bit to enable wrap RX mode for channel m. In this mode, if the RX data size is larger than channel m's RAM block size, the receiver stores the RX data from the first address to the last address in loops. (R/W)
- RMT_CONF_UPDATE_CHm: Synchronization bit for channel m. (WT)
```