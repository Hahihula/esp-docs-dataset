

```markdown
Register 44.48. LP_I2C_FIFO_CONF_REG (0x0018)
```

| Bit | Description |
|-----|-------------|
| 31-15 | (reserved) |
| 14 | `LP_I2C_FIFO_PTR_EN` |
| 13 | `LP_I2C_TX_FIFO_RST` |
| 12 | `LP_I2C_RX_FIFO_RST` |
| 11 | `(reserved)` |
| 10 | `LP_I2C_NONFIFO_EN` |
| 9-8 | `(reserved)` |
| 7 | `LP_I2C_TXFIFO_WM_THRD` |
| 6 | (reserved) |
| 5 | `LP_I2C_RXFIFO_WM_THRD` |
| 4 | Reset value: `0x2` |
| 3-0 | Reset value: `0x6` |

---

**LP_I2C_RXFIFO_WM_THRD** Configures the water mark threshold of RXFIFO in nonfifo access mode. When LP_I2C_FIFO_PTR_EN is 1 and rx FIFO counter is bigger than LP_I2C_RXFIFO_WM_THRD[4:0], LP_I2C_RXFIFO_WM_INT_RAW bit will be valid. (R/W)

**LP_I2C_TXFIFO_WM_THRD** Configures the water mark threshold of TXFIFO in nonfifo access mode. When LP_I2C_FIFO_PTR_EN is 1 and rx FIFO counter is bigger than LP_I2C_TXFIFO_WM_THRD[4:0], LP_I2C_TXFIFO_WM_INT_RAW bit will be valid. (R/W)

**LP_I2C_NONFIFO_EN** Configures to enable APB nonfifo access. (R/W)

**LP_I2C_RX_FIFO_RST** Configures to reset RXFIFO.
- 0: No effect
- 1: Reset (R/W)

**LP_I2C_TX_FIFO_RST** Configures to reset TXFIFO.
- 0: No effect
- 1: Reset (R/W)

**LP_I2C_FIFO_PTR_EN** Configures to enable FIFO pointer in non-fifo access mode. This bit controls the valid bits and the TX/RX FIFO overflow, underflow, full and empty interrupts.
- 0: No effect
- 1: Enable (R/W)
```