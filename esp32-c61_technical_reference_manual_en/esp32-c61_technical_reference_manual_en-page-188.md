

```markdown
## Register 3.27: AHB_DMA_ARB_TIMEOUT_RX_REG (0x03D0)

```
| Bit Range | Description         |
|-----------|---------------------|
| 15-0      | AHB_DMA_ARB_TIMEOUT_RX |
|           |                     |
| Reset     | 0x00                |
```

**AHB_DMA_ARB_TIMEOUT_RX** Configures the time slot for RX. Measurement unit: AHB bus clock cycle. (R/W)

## Register 3.28: AHB_DMA_WEIGHT_EN_TX_REG (0x03D4)

```
| Bit Range | Description         |
|-----------|---------------------|
| 31        |                     |
|           | (reserved)          |
| 0-0       | AHB_DMA_WEIGHT_EN_TX |
|           |                     |
| Reset     | 0                   |
```

**AHB_DMA_WEIGHT_EN_TX** Configures whether to enable weight arbitration for TX.
- 0: Disable
- 1: Enable
(R/W)

## Register 3.29: AHB_DMA_WEIGHT_EN_RX_REG (0x03D8)

```
| Bit Range | Description         |
|-----------|---------------------|
| 31        |                     |
|           | (reserved)          |
| 0-0       | AHB_DMA_WEIGHT_EN_RX |
|           |                     |
| Reset     | 0                   |
```

**AHB_DMA_WEIGHT_EN_RX** Configures whether to enable weight arbitration for RX.
- 0: Disable
- 1: Enable
(R/W)
```