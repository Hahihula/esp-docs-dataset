

```markdown
## Register 21.7 HMAC_SET_INVALIDATE_JTAG_REG (0x0060)

| Bit 31 | Description         |
|--------|---------------------|
|   0    | Reset               |

HMAC_SET_INVALIDATE_JTAG Configures whether or not to clear calculation results when re-enabling JTAG in downstream mode.
- O: Not clear
- 1: Clear calculation results (WO)

## Register 21.8 HMAC_SET_INVALIDATE_DS_REG (0x0064)

| Bit 31 | Description         |
|--------|---------------------|
|   0    | Reset               |

HMAC_SET_INVALIDATE_DS Configures whether or not to clear calculation results of the DS module in downstream mode.
- O: Not clear
- 1: Clear calculation results (WO)
```