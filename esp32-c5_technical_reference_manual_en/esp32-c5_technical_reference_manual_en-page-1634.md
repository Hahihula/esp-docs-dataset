

```markdown
Register 42.14. RMT_CHm_RX_CARRIER_RMT_RM_REG (m: 2-3) (0x0050+0x4*(m-2))

| 31 | 16   | 15    | 0     |
|----|------|-------|-------|
| 0x00 |      |       | Reset |

RMT_CARRIER_LOW_THRESH_CHm Configures the low level period in a carrier modulation mode for channel m.
The low level period in a carrier modulation mode is (RMT_CARRIER_LOW_THRESH_CHm + 1) for channel m.
Measurement unit: clk_div
(R/W)

RMT_CARRIER_HIGH_THRESH_CHm Configures the high level period in a carrier modulation mode for channel m.
The high level period in a carrier modulation mode is (RMT_CARRIER_HIGH_THRESH_CHm + 1) for channel m.
Measurement unit: clk_div
(R/W)
```