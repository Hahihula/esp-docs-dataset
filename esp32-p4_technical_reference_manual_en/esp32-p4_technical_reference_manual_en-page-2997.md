

```markdown
Register 60.11. RTC_TOUCH_DATE_REG (0x0100)

| 31 | 30 | 28 | 27 | [reserved] | RTC_CLK_EN |
|-----:|-----:|----:|----:|------------:|-----------|
|    0 |    0 |    0 |    0 |            |           |

RTC_CLK_EN Configures whether to enable the register read/write clock.
O: Disable
1: Enable
(R/W)

RTC_DATE Version control register. (R/W)
```

## 60.7.2 Configuration Registers

The addresses in this section are relative to LP Analog Peripheral base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 60.12. LP_ANA_TOUCH_APPROACH_WORK_MEAS_NUM_REG (0x00FC)

```markdown
| 31 | 30 | 29 | 20 | 19 | [reserved] | LP_ANA_TOUCH_APPROACH_MEAS_NUMO |
|-----:|-----:|----:|----:|----:|------------:|-------------------------------|
|    0 |    0 |   100 |      |   100 |            |                               |

LP_ANA_TOUCH_APPROACH_MEAS_NUM2 Configures the number of measurements for sampling frequency mode 2 in proximity mode. (R/W)

LP_ANA_TOUCH_APPROACH_MEAS_NUM1 Configures the number of measurements for sampling frequency mode 1 in proximity mode. (R/W)

LP_ANA_TOUCH_APPROACH_MEAS_NUMO Configures the number of measurements for sampling frequency mode 0 in proximity mode. (R/W)
```