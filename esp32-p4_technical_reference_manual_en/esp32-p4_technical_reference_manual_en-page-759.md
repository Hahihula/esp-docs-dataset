

```markdown
Register 10.69. LP_CLKRST_HP_USB_CLKRST_CTRL1_REG (0x0048)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  |                                             |                                                                             |
| 29  | LP_CLKRST_RST_EN_USB_OTG20_JUPL_CLK_EN     | (Reserved)                                                                   |
| 28  | LP_CLKRST_RST_EN_USB_OTG20_PHYREF_CLK_EN   | (Reserved)                                                                   |
| 27  | LP_CLKRST_RST_EN_USB_OTG20_PHYREF_CLK_SRC_SEL | (Reserved)                                                                   |
| 5   |                                             |                                                                             |
| 4   | LP_CLKRST_RST_EN_USB_DEVICE                | Configures whether to reset USB Serial/JTAG.                                |
| 3   | LP_CLKRST_RST_EN_USB_OTGT1                  | Configures whether to reset Full-Speed USB 2.0 OTG.                          |
| 2   | LP_CLKRST_RST_EN_USB_OTG20_ADp             | Configures whether to reset High-Speed USB 2.0 OTG ADP.                      |
| 1   |                                             |                                                                             |
| 0   | Reset                                      |                                                                             |

LP_CLKRST_RST_EN_USB_OTG20_ADp Configures whether to reset High-Speed USB 2.0 OTG ADP.
    0: Release from reset
    1: Reset (R/W)

LP_CLKRST_RST_EN_USB_OTG20_PHY Configures whether to reset High-Speed USB 2.0 OTG PHY.
    0: Release from reset
    1: Reset (R/W)

LP_CLKRST_RST_EN_USB_OTG20 Configures whether to reset High-Speed USB 2.0 OTG.
    0: Release from reset
    1: Reset (R/W)

LP_CLKRST_RST_EN_USB_OTGT1 Configures whether to reset Full-Speed USB 2.0 OTG.
    0: Release from reset
    1: Reset (R/W)

LP_CLKRST_RST_EN_USB_DEVICE Configures whether to reset USB Serial/JTAG.
    0: Release from reset
    1: Reset (R/W)

Continued on the next page...
```