

```markdown
Register 25.7. RSA_CONSTANT_TIME_REG (0x0820)

| Bit 31 | 31:0 | Description |
|--------|-------|-------------|
|       |      | (reserved)  |
|       |      |             |
|       |      | RSA_CONSTANT_TIME |

RSA_CONSTANT_TIME Configures the CONSTANT_TIME option.
- O: Acceleration
- 1: No acceleration (default)
(R/W)

Register 25.8. RSA_SEARCH_ENABLE_REG (0x0824)

| Bit 31 | 31:0 | Description |
|--------|-------|-------------|
|       |      | (reserved)  |
|       |      |             |
|       |      | RSA_SEARCH_ENABLE |

RSA_SEARCH_ENABLE Configures the SEARCH option.
- O: No acceleration (default)
- 1: Acceleration
This option should be used together with RSA_SEARCH_POS_REG.
(R/W)

Register 25.9. RSA_SEARCH_POS_REG (0x0828)

| Bit 31 | 31:12 | 11:0 | Description |
|--------|-------|------|-------------|
|       |      |     | (reserved)  |
|       |      |     |             |
|       |      |     | RSA_SEARCH_POS |

RSA_SEARCH_POS Configures the starting address to start search.
This field should be used together with RSA_SEARCH_ENABLE_REG. The field is only valid when RSA_SEARCH_ENABLE is 1.
(R/W)
```