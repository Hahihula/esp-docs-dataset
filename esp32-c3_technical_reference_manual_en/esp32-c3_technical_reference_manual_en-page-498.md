

```markdown
## Register 19.7 HMAC_SET_INVALIDATE_JTAG_REG (0x0060)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| ... |             |
| 0   | Reset       |

**HMAC_SET_INVALIDATE_JTAG** Set this bit to clear calculation results when re-enabling JTAG in downstream mode. (WO)


## Register 19.8 HMAC_SET_INVALIDATE_DS_REG (0x0064)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| ... |             |
| 0   | Reset       |

**HMAC_SET_INVALIDATE_DS** Set this bit to clear calculation results of the DS module in downstream mode. (WO)


## Register 19.9 HMAC_QUERY_ERROR_REG (0x0068)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| ... |             |
| 0   | Reset       |

**HMAC_QUERY_CHECK** Indicates whether an HMAC key matches the purpose.(RO)
*   0: HMAC key and purpose match.
*   1: error.
```