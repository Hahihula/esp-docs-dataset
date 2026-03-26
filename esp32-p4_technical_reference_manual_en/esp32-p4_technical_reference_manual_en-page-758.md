

```markdown
Register 10.68. LP_CLKRST_HP_USB_CLKRST_CTRL0_REG (0x0044)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0   | 0  |    |    |    |    |    |    |    |    |    |    |    |    |    | LP_CLKRST_USB_12M_DIV_NUM | reserved | LP_CLKRST_USB_48M_DIV_NUM | LP_CLKRST_USB_25M_DIV_NUM | LP_CLKRST_USB_DEVICE_48M_CLK_EN | LP_CLKRST_USB_OTG11_BK_SYS_CLK_EN | LP_CLKRST_USB_OTG20_BK_SYS_CLK_EN | LP_CLKRST_USB_OTG20_SLEEP_MODE | Reset |

LP_CLKRST_USB_OTG20_SLEEP_MODE  Not used. (R/W)

LP_CLKRST_USB_OTG20_BK_SYS_CLK_EN  Not used. (R/W)

LP_CLKRST_USB_OTG11_SLEEP_MODE  Not used. (R/W)

LP_CLKRST_USB_OTG11_BK_SYS_CLK_EN  Not used. (R/W)

LP_CLKRST_USB_OTG11_48M_CLK_EN  Configures whether to enable the Full-Speed USB 2.0 OTG PHY clock.
    0: Disable
    1: Enable
    (R/W)

LP_CLKRST_USB_DEVICE_48M_CLK_EN  Configures whether to enable the USB Serial/JTAG PHY clock.
    0: Disable
    1: Enable
    (R/W)

LP_CLKRST_USB_48M_DIV_NUM  Configures the division number from USB 480M to 25M. (R/W)

LP_CLKRST_USB_25M_DIV_NUM  Configures the division number from USB 500M to 25M. (R/W)

LP_CLKRST_USB_12M_DIV_NUM  Configures the division number from USB 480M to 12M. (R/W)
```