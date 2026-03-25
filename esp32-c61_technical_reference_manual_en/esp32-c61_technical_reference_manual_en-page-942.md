

```markdown
Register 26.13. SPI_CLK_GATE_REG (0x00E8)
```

| Bit | Description |
|-----|-------------|
| 3   | SPI_MST_CLK_SEL |
| 2   | SPI_MST_CLK_ACTIVE |
| 1   | SPI_CLK_EN |
| 0   | Reset |

```markdown
SPI_CLK_EN Configures whether or not to enable clock gate.
O: Disable
1: Enable
(R/W)

SPI_MST_CLK_ACTIVE Set this bit to power on the SPI module clock. (R/W)

SPI_MST_CLK_SEL This bit is used to select SPI module clock source in master mode. 1: PLL_CLK_80M. 0: XTAL CLK. (R/W)
```