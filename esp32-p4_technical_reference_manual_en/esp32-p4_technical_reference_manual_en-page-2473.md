

# 46.15 Registers

The addresses in this section are relative to I2Sn base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 46.1: I2S_INT_RAW_REG (0x000C)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 3   | I2S_TX_HUNG_INT_RAW |
| 2   | I2S_RX_HUNG_INT_RAW |
| 1   | I2S_TX_DONE_INT_RAW |
| 0   | I2S_RX_DONE_INT_RAW |

- **I2S_RX_DONE_INT_RAW** The raw interrupt status of the I2S_RX_DONE_INT interrupt. (R/SS/WTC)
- **I2S_TX_DONE_INT_RAW** The raw interrupt status of the I2S_TX_DONE_INT interrupt. (R/SS/WTC)
- **I2S_RX_HUNG_INT_RAW** The raw interrupt status of the I2S_RX_HUNG_INT interrupt. (R/SS/WTC)
- **I2S_TX_HUNG_INT_RAW** The raw interrupt status of the I2S_TX_HUNG_INT interrupt. (R/SS/WTC)

## Register 46.2: I2S_INT_ST_REG (0x0010)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 3   | I2S_TX_HUNG_INT_ST |
| 2   | I2S_RX_HUNG_INT_ST |
| 1   | I2S_TX_DONE_INT_ST |
| 0   | I2S_RX_DONE_INT_ST |

- **I2S_RX_DONE_INT_ST** The masked interrupt status of the I2S_RX_DONE_INT interrupt. (RO)
- **I2S_TX_DONE_INT_ST** The masked interrupt status of the I2S_TX_DONE_INT interrupt. (RO)
- **I2S_RX_HUNG_INT_ST** The masked interrupt status of the I2S_RX_HUNG_INT interrupt. (RO)
- **I2S_TX_HUNG_INT_ST** The masked interrupt status of the I2S_TX_HUNG_INT interrupt. (RO)