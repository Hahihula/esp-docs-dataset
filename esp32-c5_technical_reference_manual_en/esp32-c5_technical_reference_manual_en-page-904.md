

```markdown
## 24.6.4 Registers

The addresses in this section are relative to HMAC Accelerator base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 24.1. HMAC_SET_START_REG (0x0040)

```markdown
| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|       |     | Reset |    |
```

**HMAC_SET_START**: Configures whether or not to enable HMAC.
- O: Disable HMAC
- 1: Enable HMAC
(WS)

### Register 24.2. HMAC_SET_PARA_FINISH_REG (0x004C)

```markdown
| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|       |     | Reset |    |
```

**HMAC_SET_PARA_END**: Configures whether to finish HMAC configuration.
- O: No effect
- 1: Finish configuration
(WS)

### Register 24.3. HMAC_SET_MESSAGE_ONE_REG (0x0050)

```markdown
| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|       |     | Reset |    |
```

**HMAC_SET_TEXT_ONE**: Calls SHA to calculate one message block. (WS)
```