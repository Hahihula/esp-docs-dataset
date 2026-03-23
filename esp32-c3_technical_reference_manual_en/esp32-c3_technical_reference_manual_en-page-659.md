

```markdown
Register 27.13. SPI_CLK_GATE_REG (0x00E8)
```

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 3   | SPI_MST_CLK_SEL    | This bit is used to select SPI module clock source in master mode. 1: PLL_F80M_CLK, 0: XTAL_CLK. (R/W) |
| 2   | SPI_MST_CLK_ACTIVE | Set this bit to power on the SPI module clock. (R/W)                         |
| 1   | SPI_CLK_EN         | Set this bit to enable clock gate. (R/W)                                    |
| 0-31| (reserved)         |                                                                             |

```markdown
SPI_CLK_EN    Set this bit to enable clock gate. (R/W)
SPI_MST_CLK_ACTIVE    Set this bit to power on the SPI module clock. (R/W)
SPI_MST_CLK_SEL    This bit is used to select SPI module clock source in master mode. 1: PLL_F80M_CLK, 0: XTAL_CLK. (R/W)
```