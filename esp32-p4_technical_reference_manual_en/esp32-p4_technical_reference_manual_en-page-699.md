

```markdown
Register 10.33. HP_SYS_CLKRST_PERI_CLK_CTRL116_REG (0x0080)

| Bit | Field Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                  | -                                                                                                                                          |
| 25  | HP_SYS_CLKRST_GPSPI2_CLK_SRC_SEL                                          | Configures the clock source for GPSPI2_CLK. <br> O: XTAL_CLK<br> 1: RC_FAST_CLK<br> 2: SDIO_PLLO_CLK<br> 3: APLL_CLK<br> 4: SPLL_CLK (480 MHz)<br> 5-7: Invalid (R/W) |
| 24  | HP_SYS_CLKRST_GPSPI2_HS_CLK_EN                                           | Configures whether to enable GPSPI2_HS_CLK. <br> O: Disable<br> 1: Enable (R/W)                                                             |
| 23  | HP_SYS_CLKRST_GPSPI2_HS_CLK_DIV_NUM                                     | Configures the integer part of the clock divisor of GPSPI2_HS_CLK. (R/W)                                                                   |
| 22  | HP_SYS_CLKRST_GPSPI2_MST_CLK_DIV_NUM                                    | Configures the integer part of the clock divisor of GPSPI2_MST_CLK. (R/W)                                                                  |
| 21  | HP_SYS_CLKRST_GPSPI2_MST_CLK_EN                                         | Configures whether to enable GPSPI2_MST_CLK. <br> O: Disable<br> 1: Enable (R/W)                                                             |
| 20  | HP_SYS_CLKRST_GPSPI3_CLK_SRC_SEL                                        | Configures the clock source for GPSPI3_CLK. <br> O: XTAL_CLK<br> 1: RC_FAST_CLK<br> 2: SDIO_PLLO_CLK<br> 3: APLL_CLK<br> 4: SPLL_CLK (480 MHz)<br> 5-7: Invalid (R/W) |
| 19  | HP_SYS_CLKRST_GPSPI3_HS_CLK_EN                                         | Configures whether to enable GPSPI3_HS_CLK. <br> O: Disable<br> 1: Enable (R/W)                                                             |

Reset values:
Bit 20: 1
Bit 19: 1
Bit 18-0: 0

```
```markdown
Chapter 10 Reset and Clock
GoBack

HP_SYS_CLKRST_GPSPI2_CLK_SRC_SEL Configures the clock source for GPSPI2_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
2: SDIO_PLLO_CLK
3: APLL_CLK
4: SPLL_CLK (480 MHz)
5-7: Invalid
(R/W)

HP_SYS_CLKRST_GPSPI2_HS_CLK_EN Configures whether to enable GPSPI2_HS_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_GPSPI2_HS_CLK_DIV_NUM Configures the integer part of the clock divisor of GPSPI2_HS_CLK. (R/W)

HP_SYS_CLKRST_GPSPI2_MST_CLK_DIV_NUM Configures the integer part of the clock divisor of GPSPI2_MST_CLK. (R/W)

HP_SYS_CLKRST_GPSPI2_MST_CLK_EN Configures whether to enable GPSPI2_MST_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_GPSPI3_CLK_SRC_SEL Configures the clock source for GPSPI3_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
2: SDIO_PLLO_CLK
3: APLL_CLK
4: SPLL_CLK (480 MHz)
5-7: Invalid
(R/W)

HP_SYS_CLKRST_GPSPI3_HS_CLK_EN Configures whether to enable GPSPI3_HS_CLK.
O: Disable
1: Enable
(R/W)

Espressif Systems

699
ESP32-P4 TRM
PRELIMINARY
Submit Documentation Feedback
```