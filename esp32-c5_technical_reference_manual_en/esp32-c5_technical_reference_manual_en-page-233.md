

```markdown
Register 5.48. AHB_DMA_MODULE_CLK_EN_REG (0x0404)

Continued from the previous page...

AHB_DMA_CMD_ARB_CLK_EN Configures whether to forcibly enable the clock for the GDMA arbitration module.
O: Not forcibly enable
1: Forcibly enable
(R/W)

AHB_DMA_AHBINF_CLK_EN Configures whether to forcibly enable the clock for the GDMA bus interface processing module.
O: Not forcibly enable
1: Forcibly enable
(R/W)

Register 5.49. AHB_DMA_AHBINF_RESP_ERR_STATUSO_REG (0x0408)
```
```markdown
| 31 | 0 |
|----|---|
|    |   |
| 0x0 | Reset |

AHB_DMA_AHBINF_RESP_ERR_ADDR Represents the address of the current AHB bus transfer that triggers an error response. (RO)
```