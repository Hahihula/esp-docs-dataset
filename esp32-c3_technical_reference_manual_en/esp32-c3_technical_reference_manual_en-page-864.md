

```markdown
Register 33.14. RMT_CHnCARRIER_DUTY_REG (n = 0, 1) (0x0048, 0x004C)

| 31           | 16   | 15       | 0         |
|--------------|------|----------|-----------|
|              |      |          | Reset     |
| 0x40         |       | 0x40     |           |

RMT_CARRIER_LOW_CHn
channel n. (R/W)

This field is used to configure carrier wave's low level clock period for channel n.

RMT_CARRIER_HIGH_CHn
channel n. (R/W)

This field is used to configure carrier wave's high level clock period for channel n.

Register 33.15. RMT_CHm_RX_CARRIER_RM_REG (m = 2, 3) (0x0050, 0x0054)

| 31           | 16   | 15       | 0         |
|--------------|------|----------|-----------|
|              |      |          | Reset     |
| 0x00         |       | 0x00     |           |

RMT_CARRIER_LOW_THRES_CHm
(RMT_CARRIER_LOW_THRES_CHm + 1) for channel m. (R/W)

RMT_CARRIER_HIGH_THRES_CHm
(RMT_CARRIER_HIGH_THRES_CHm + 1) for channel m. (R/W)
```