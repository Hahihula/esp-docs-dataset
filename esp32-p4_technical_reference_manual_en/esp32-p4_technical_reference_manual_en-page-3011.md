

# Chapter 60 Touch Sensor (TOUCH)

GoBack

## Register 60.31. LP_ANA_TOUCH_CTRL_REG (0x01FC)

LP_ANA_TOUCH_UPDATE_BENCHMARK_FREQ_SEL Configures the frequency point used by software to update the benchmark. (R/W)

LP_ANA_TOUCH_UPDATE_BENCHMARK_PAD_SEL Configures the channel used by software to update the benchmark. (R/W)

LP_ANA_FREQ_SCAN_CNT_RISE Configures the number of hit frequency points to be evaluated for touch detection in frequency hopping mode. (R/W)

## Register 60.32. LP_ANA_DATE_REG (0x03FC)

LP_ANA_CLK_EN

| 31 | 30 | ... | 0 |
|----:|----:|-----|---|
|   O |    |     | Reset |

LP_ANA_LP_ANA_DATE 0x250220

LP_ANA_LP_ANA_DATE Version control register. (R/W)

LP_ANA_CLK_EN Configures whether to enable the clock for accessing the registers.
O: Disable
1: Enable
(R/W)