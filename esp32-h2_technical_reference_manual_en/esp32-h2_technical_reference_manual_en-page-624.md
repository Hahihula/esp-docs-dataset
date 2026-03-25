

```markdown
Chapter 21 HMAC Accelerator (HMAC)

Register 21.4. HMAC_SET_MESSAGE_ING_REG (0x0054)


HMAC_SET_TEXT_ING Configures whether there are unprocessed message blocks.
O: No unprocessed message block
1: There are still some message blocks to be processed.
(WO)

Register 21.5. HMAC_SET_MESSAGE_END_REG (0x0058)


HMAC_SET_TEXT_END Configures whether to start hardware padding.
O: No effect
1: Start hardware padding
(WO)

Register 21.6. HMAC_SET_RESULT_FINISH_REG (0x005C)


HMAC_SET_RESULT_END Configures whether to exit upstream mode and clear calculation results.
O: No effect
1: Exit upstream mode and clear calculation results.
(WO)
```