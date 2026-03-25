

```markdown
Register 39.3. HINF_CFG_DATA7_REG (0x001C)

| (reserved) | HINF_SDIO_WAKEUP_CLR | HINF_ESDIO_DATA1_INT_EN | HINF_SDIO_RST | HINF_CHIP_STATE | HINF_PIN_STATE |
|:-----------:|:---------------------:|:------------------------:|:-------------:|:---------------:|:--------------:|
| 31          |        30             |           29            |       20      |         8       |                |
|             |                      |                         |              |                 |               |
|     0x238   |                        |                          |               |                 | Reset          |

HINF_PIN_STATE Configures SDIO CIS address 318 and 574. Please refer to SDIO Specification for details. (R/W)

HINF_CHIP_STATE Configures SDIO CIS address 312, 315, 568, and 571. Please refer to SDIO Specification for details. (R/W)

HINF_SDIO_RST Configures whether to reset the SDIO slave module.
O: No effect
1: Reset
(R/W)

HINF_ESDIO_DATA1_INT_EN Configures whether to enable SDIO interrupt on data1 line.
O: Disable
1: Enable
(R/W)

HINF_SDIO_WAKEUP_CLR Configures whether to clear wake up signal after the chip is waken up by the SDIO slave.
O: No effect
1: Clear
(WT)
```

Register 39.4. HINF_CIS_CONF_Wn_REG(n: 0-7) (0x0020+0x4*n)

| 31 | Oxffffffff | Reset |
|----|------------|-------|
```markdown
HINF_CIS_CONF_Wn Configures SDIO CIS address (39+4*n) ~ (36+4*n). Please refer to SDIO Specification for details. (R/W)
```