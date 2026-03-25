

# 31.15 Registers

The addresses in this section are relative to the I2S Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 31.1. I2S_INT_RAW_REG (0x000C)

| Bit | Description |
|-----|-------------|
| 31:0 | (reserved) |

- **I2S_RX_DONE_INT_RAW** The raw interrupt status of the `I2S_RX_DONE_INT` interrupt. (R/SS/WTC)
- **I2S_TX_DONE_INT_RAW** The raw interrupt status of the `I2S_TX_DONE_INT` interrupt. (R/SS/WTC)
- **I2S_RX_HUNG_INT_RAW** The raw interrupt status of the `I2S_RX_HUNG_INT` interrupt. (R/SS/WTC)
- **I2S_TX_HUNG_INT_RAW** The raw interrupt status of the `I2S_TX_HUNG_INT` interrupt. (R/SS/WTC)

## Register 31.2. I2S_INT_ST_REG (0x0010)

| Bit | Description |
|-----|-------------|
| 31:0 | (reserved) |

- **I2S_RX_DONE_INT_ST** The masked interrupt status of the `I2S_RX_DONE_INT` interrupt. (RO)
- **I2S_TX_DONE_INT_ST** The masked interrupt status of the `I2S_TX_DONE_INT` interrupt. (RO)
- **I2S_RX_HUNG_INT_ST** The masked interrupt status of the `I2S_RX_HUNG_INT` interrupt. (RO)
- **I2S_TX_HUNG_INT_ST** The masked interrupt status of the `I2S_TX_HUNG_INT` interrupt. (RO)