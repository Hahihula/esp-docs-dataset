

```markdown
Register 4.102. AXI_DMA_ARB_TIMEOUT_REG (0x0270)

| 31 | 16   | 15    | 0     |
|----|------|-------|-------|
|    |      |       | Reset |
| 0x00 |      | 0x00  |

AXI_DMA_ARB_TIMEOUT_TX Configures the time slot for TX. Measurement unit: AXI bus clock cycle. (R/W)

AXI_DMA_ARB_TIMEOUT_RX Configures the time slot for RX. Measurement unit: AXI bus clock cycle. (R/W)


Register 4.103. AXI_DMA_WEIGHT_EN_REG (0x0274)

| 31 | ... (reserved) | 2 | 1 | 0 |
|----|-----------------|---|---|---|
|    |                 |   | Reset |

AXI_DMA_WEIGHT_EN_TX Configures whether to enable weight arbitration for TX.
O: Disable
1: Enable
(R/W)

AXI_DMA_WEIGHT_EN_RX Configures whether to enable weight arbitration for RX.
O: Disable
1: Enable
(R/W)
```