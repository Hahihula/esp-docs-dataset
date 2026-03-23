

# 29.14 Registers

## Register 29.1. I2S_INT_RAW_REG (0x000C)

```
31
+---------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |
+---------------------------------------------------------------+
```

- **I2S_RX_DONE_INT_RAW** The raw interrupt status bit for I2S_RX_DONE_INT interrupt. (RO/WTC/SS)
- **I2S_TX_DONE_INT_RAW** The raw interrupt status bit for I2S_TX_DONE_INT interrupt. (RO/WTC/SS)
- **I2S_RX_HUNG_INT_RAW** The raw interrupt status bit for I2S_RX_HUNG_INT interrupt. (RO/WTC/SS)
- **I2S_TX_HUNG_INT_RAW** The raw interrupt status bit for I2S_TX_HUNG_INT interrupt. (RO/WTC/SS)

## Register 29.2. I2S_INT_ST_REG (0x0010)

```
31
+---------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |
+---------------------------------------------------------------+
```

- **I2S_RX_DONE_INT_ST** The masked interrupt status bit for I2S_RX_DONE_INT interrupt. (RO)
- **I2S_TX_DONE_INT_ST** The masked interrupt status bit for I2S_TX_DONE_INT interrupt. (RO)
- **I2S_RX_HUNG_INT_ST** The masked interrupt status bit for I2S_RX_HUNG_INT interrupt. (RO)
- **I2S_TX_HUNG_INT_ST** The masked interrupt status bit for I2S_TX_HUNG_INT interrupt. (RO)