

```markdown
Chapter 38 Controller Area Network Flexible Data-Rate (CAN FD)

Register 38.37. TWAIFD_FILTER_B_VAL_REG (0x0048)
```

| 31 | 29 | 28 | [reserved] | 0 |
|----:|----:|----:|-----------:|---|
|   0 |   0 |   0 |            | Reset |

TWAIFD_BIT_VAL_B_VAL Configures filter B bit value. The identifier format is the same as in IDENTIFIER_W of the TX or RX buffer. If filter B is not present, writes to this register have no effect and reads will return all zeroes. (R/W)

Register 38.38. TWAIFD_FILTER_C_MASK_REG (0x004C)
```

| 31 | 29 | 28 | [reserved] | 0 |
|----:|----:|----:|-----------:|---|
|   0 |   0 |   0 |            | Reset |

TWAIFD_BIT_MASK_C_VAL Configures filter C masked value. The identifier format is the same as in IDENTIFIER_W of the TX or RX buffer. If filter C is not present, writes to this register have no effect and reads will return all zeroes. (R/W)

Register 38.39. TWAIFD_FILTER_C_VAL_REG (0x0050)
```

| 31 | 29 | 28 | [reserved] | 0 |
|----:|----:|----:|-----------:|---|
|   0 |   0 |   0 |            | Reset |

TWAIFD_BIT_VAL_C_VAL Configures filter C bit value. The identifier format is the same as in IDENTIFIER_W of the TX or RX buffer. If filter A is not present, writes to this register have no effect and reads will return all zeroes. (R/W)
```