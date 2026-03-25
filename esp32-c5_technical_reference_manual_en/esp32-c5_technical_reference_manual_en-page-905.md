

```markdown
Chapter 24 HMAC Accelerator (HMAC)

Register 24.4. HMAC_SET_MESSAGE_ING_REG (0x0054)
```

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| ... |             |
| 0   | Reset       |

```markdown
HMAC_SET_TEXT_ING Configures whether or not there are unprocessed message blocks.
0: No unprocessed message block
1: There are still some message blocks to be processed.
(WS)
```

```markdown
Register 24.5. HMAC_SET_MESSAGE_END_REG (0x0058)
```

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| ... |             |
| 0   | Reset       |

```markdown
HMAC_SET_TEXT_END Configures whether to start hardware padding.
0: No effect
1: Start hardware padding
(WS)
```

```markdown
Register 24.6. HMAC_SET_RESULT_FINISH_REG (0x005C)
```

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| ... |             |
| 0   | Reset       |

```markdown
HMAC_SET_RESULT_END Configures whether to exit upstream mode and clear calculation results.
0: Not exit
1: Exit upstream mode and clear calculation results.
(WS)
```

Espressif Systems

905

ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```