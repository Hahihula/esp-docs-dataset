

```markdown
Chapter 27 HMAC Accelerator (HMAC)

Register 27.3. HMAC_SET_MESSAGE_ONE_REG (0x0050)
```

| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|        |     |   | Reset |

**HMAC_SET_TEXT_ONE** Calls SHA to calculate one message block.

- O: No effect
- 1: Calls SHA to calculate one message block.
(WO)

Register 27.4. HMAC_SET_MESSAGE_ING_REG (0x0054)
```

| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|        |     |   | Reset |

**HMAC_SET_TEXT_ING** Configures whether or not there are unprocessed message blocks.

- O: No unprocessed message block
- 1: There are still some message blocks to be processed.
(WO)

Register 27.5. HMAC_SET_MESSAGE_END_REG (0x0058)
```

| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|        |     |   | Reset |

**HMAC_SET_TEXT_END** Configures whether to start hardware padding.

- O: No effect
- 1: Start hardware padding
(WO)
```