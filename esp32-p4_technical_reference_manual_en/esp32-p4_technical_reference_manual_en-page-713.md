

```markdown
Register 10.44. HP_SYS_CLKRST_PERI_CLK_CTRL26_REG (0x00AC)

| 31 | 28 | 27 | 20 | 19 | 18 | 17 | 10 | 9 | 8 | 7 | 0 |
|-----|-----|-----|----|----|----|----|----|---|---|---|---|
| 0   | 0   | 0   | 0  | 0  | 0  | O  | 1  | 0 | O | Reset |

HP_SYS_CLKRST_ISP_CLK_DIV_NUM Configures the clock divisor of ISP_CLK. (R/W)

HP_SYS_CLKRST_IOMUX_CLK_SRC_SEL Configures the clock source for IOMUX_CLK.
O: XTAL_CLK
1: PLL_F80M_CLK
(R/W)

HP_SYS_CLKRST_IOMUX_CLK_EN Configures whether to enable the IOMUX_CLK clock.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_IOMUX_CLK_DIV_NUM Configures the clock divisor of IOMUX_CLK. (R/W)

HP_SYS_CLKRST_H264_CLK_SRC_SEL Configures the clock source for H264_CLK.
O: XTAL_CLK
1: PLL_F240M_CLK
(R/W)

HP_SYS_CLKRST_H264_CLK_EN Configures whether to enable the H264_CLK clock.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_H264_CLK_DIV_NUM Configures the clock divisor of H264_CLK. (R/W)
```