

```markdown
## 30.15 Registers

The addresses in this section are relative to I2S Controller base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 30.1. I2S_INT_RAW_REG (0x000C)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 4   | I2S_TX_HUNG_INT_RAW         | The raw interrupt status of the `I2S_TX_HUNG_INT` interrupt.                 |
| 3   | I2S_RX_HUNG_INT_RAW         | The raw interrupt status of the `I2S_RX_HUNG_INT` interrupt.                 |
| 2   | I2S_TX_DONE_INT_RAW         | The raw interrupt status of the `I2S_TX_DONE_INT` interrupt.                 |
| 1   | I2S_RX_DONE_INT_RAW         | The raw interrupt status of the `I2S_RX_DONE_INT` interrupt.                 |
| 0   |                             | Reset                                                                        |

- **I2S_RX_DONE_INT_RAW**: The raw interrupt status of the `I2S_RX_DONE_INT` interrupt. (RO/WTC/SS)
- **I2S_TX_DONE_INT_RAW**: The raw interrupt status of the `I2S_TX_DONE_INT` interrupt. (RO/WTC/SS)
- **I2S_RX_HUNG_INT_RAW**: The raw interrupt status of the `I2S_RX_HUNG_INT` interrupt. (RO/WTC/SS)
- **I2S_TX_HUNG_INT_RAW**: The raw interrupt status of the `I2S_TX_HUNG_INT` interrupt. (RO/WTC/SS)

### Register 30.2. I2S_INT_ST_REG (0x0010)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 4   | I2S_TX_HUNG_INT_ST          | The masked interrupt status of the `I2S_TX_HUNG_INT` interrupt.              |
| 3   | I2S_RX_HUNG_INT_ST          | The masked interrupt status of the `I2S_RX_HUNG_INT` interrupt.              |
| 2   | I2S_TX_DONE_INT_ST          | The masked interrupt status of the `I2S_TX_DONE_INT` interrupt.              |
| 1   | I2S_RX_DONE_INT_ST          | The masked interrupt status of the `I2S_RX_DONE_INT` interrupt.              |
| 0   |                             | Reset                                                                        |

- **I2S_RX_DONE_INT_ST**: The masked interrupt status of the `I2S_RX_DONE_INT` interrupt. (RO)
- **I2S_TX_DONE_INT_ST**: The masked interrupt status of the `I2S_TX_DONE_INT` interrupt. (RO)
- **I2S_RX_HUNG_INT_ST**: The masked interrupt status of the `I2S_RX_HUNG_INT` interrupt. (RO)
- **I2S_TX_HUNG_INT_ST**: The masked interrupt status of the `I2S_TX_HUNG_INT` interrupt. (RO)
```