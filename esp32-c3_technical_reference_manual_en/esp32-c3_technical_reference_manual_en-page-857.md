

```markdown
## Register 33.6. RMT_SYS_CONF_REG (0x0068)

| Bit | Field Name                  | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 31  | RMT_CLK_EN                   | The enable signal of RMT register clock gate. 1: Power up the drive clock of registers.<br>0: Power down the drive clock of registers. (R/W) |
| 30  | (reserved)                  |                                                                             |
| 27  |                              |                                                                             |
| 26  |                              |                                                                             |
| 25  | RMT_SCLK_ACTIVE              | RMT_SCLK_ACTIVE                                                              |
| 24  | RMT_SCLK_SEL                 | Choose the clock source of rmt_sclk. 1: APB_CLK; 2: RC_FAST_CLK; 3: XTAL_CLK. (R/W) |
| 23  |                              |                                                                             |
| 22  |                              |                                                                             |
| 18  | RMT_SCLK_DIV_B               | The denominator of the fractional part of the fractional divider. (R/W)      |
| 17  | RMT_SCLK_DIV_A               | The numerator of the fractional part of the fractional divider. (R/W)        |
| 12  |                              |                                                                             |
| 11  | RMT_SCLK_DIV_NUM             | The integral part of the fractional divider. (R/W)                           |
| 4   |                              |                                                                             |
| 3   |                              |                                                                             |
| 2   |                              |                                                                             |
| 1   |                              |                                                                             |
| 0   | Reset                        | 0x0                                                                            |

- RMT_APB_FIFO_MASK    1'h1: Access memory directly. 1'h0: Access memory by FIFO. (R/W)
- RMT_MEM_CLK_FORCE_ON  Set this bit to enable the clock for RMT memory. (R/W)
- RMT_MEM_FORCE_PD      Set this bit to power down RMT memory. (R/W)
- RMT_MEM_FORCE_PU      1: Disable the power-down function of RMT memory in Light-sleep.<br>0: Power down RMT memory when RMT is in Light-sleep mode. (R/W)

## Register 33.7. RMT_REF_CNT_RST_REG (0x0070)

| Bit | Field Name                  | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                  |                                                                             |
| 4   |                              |                                                                             |
| 3   |                              |                                                                             |
| 2   |                              |                                                                             |
| 1   |                              |                                                                             |
| 0   | Reset                        | 0x0                                                                            |

- RMT_REF_CNT_RST_CHO    This bit is used to reset the clock divider of channel 0. (WT)
- RMT_REF_CNT_RST_CH1    This bit is used to reset the clock divider of channel 1. (WT)
- RMT_REF_CNT_RST_CH2    This bit is used to reset the clock divider of channel 2. (WT)
- RMT_REF_CNT_RST_CH3    This bit is used to reset the clock divider of channel 3. (WT)
```