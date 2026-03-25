

```markdown
Chapter 21 HMAC Accelerator (HMAC)

Register 21.15. HMAC_SET_MESSAGE_PAD_REG (0x00F0)
```

![Register 21.15 Bit Diagram](image_description: A bit field diagram for register HMAC_SET_MESSAGE_PAD_REG (0x00F0). The top row shows bits from 31 to 0, with the rightmost two bits labeled as "Reset" and "reserved". The bit at position 1 is labeled "HMAC_SET_TEXT_PAD".)

```markdown
HMAC_SET_TEXT_PAD Configures whether the padding is applied by software.
O: Not applied by software
1: Applied by software
(WO)
```

Register 21.16. HMAC_ONE_BLOCK_REG (0x00F4)

![Register 21.16 Bit Diagram](image_description: A bit field diagram for register HMAC_ONE_BLOCK_REG (0x00F4). The top row shows bits from 31 to 0, with the rightmost two bits labeled as "Reset" and "reserved". The bit at position 1 is labeled "HMAC_SET_ONE_BLOCK".)

```markdown
HMAC_SET_ONE_BLOCK Write 1 to indicate Block_1 is the only one block, and Block_1 contains all the padding bits and there is no need for padding. (WO)
```

Register 21.17. HMAC_SOFT_JTAG_CTRL_REG (0x00F8)

![Register 21.17 Bit Diagram](image_description: A bit field diagram for register HMAC_SOFT_JTAG_CTRL_REG (0x00F8). The top row shows bits from 31 to 0, with the rightmost two bits labeled as "Reset" and "reserved". The bit at position 1 is labeled "HMAC_SOFT_JTAG_CTRL".)

```markdown
HMAC_SOFT_JTAG_CTRL Configures whether to enable JTAG authentication mode.
O: Disable
1: Enable
(WO)
```

Espressif Systems

628

ESP32-H2 TRM (Version 1.1)

Submit Documentation Feedback
```