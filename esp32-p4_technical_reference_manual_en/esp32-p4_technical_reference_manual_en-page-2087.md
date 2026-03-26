

```markdown
Register 40.17: CSI_HOST_INT_FORCE_PKT_FATAL_REG (0x00F8)

| Bit 31 | ... | 2 | 1 | 0 |
|--------|-----|---|---|---|
|        |     |   |   | Reset |

CSI_HOST_FORCE_ERR_ECC_DOUBLE Configures whether to force set CSI_HOST_ST_ERR_ECC_DOUBLE to 1.
- 0: Do not force set
- 1: Force set
(R/W)

CSI_HOST_FORCE_SHORTER_PAYLOAD Configures whether to force set CSI_HOST_ST_SHORTER_PAYLOAD to 1.
- 0: Do not force set
- 1: Force set
(R/W)
```