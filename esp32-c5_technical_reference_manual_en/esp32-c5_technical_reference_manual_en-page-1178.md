

```markdown
Register 33.13. SPI_CLK_GATE_REG (0x00E8)
```

```text
(reserved)           (reserved)          SPI_CLK_EN
                     3   2   1   0
-------------------------------------------------
31                   |   |   |   |
-------------------------------------------------
0                    0   0   0   0 Reset
```

```markdown
SPI_CLK_EN Configures whether or not to enable clock gate.
O: Disable
1: Enable
(R/W)
```