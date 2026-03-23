

```markdown
Chapter 21 HMAC Accelerator (HMAC)

Register 21.15. HMAC_SET_MESSAGE_PAD_REG (0x00F0)
```

![Register 21.15 Bit Diagram](image_description: A bit field diagram for HMAC_SET_MESSAGE_PAD_REG showing all bits as 'reserved' except the least significant bit labeled "Reset" with value 0, and a note indicating "HMAC_SET_TEXT_PAD".)

```markdown
HMAC_SET_TEXT_PAD Configures whether or not the padding is applied by software.
O: Not applied by software
1: Applied by software
(WO)
```

Register 21.16. HMAC_ONE_BLOCK_REG (0x00F4)

![Register 21.16 Bit Diagram](image_description: A bit field diagram for HMAC_ONE_BLOCK_REG showing all bits as 'reserved' except the least significant bit labeled "Reset" with value 0, and a note indicating "HMAC_SET_ONE_BLOCK".)

```markdown
HMAC_SET_ONE_BLOCK Write 1 to indicate there is only one block which already contains padding bits and there is no need for padding. (WO)
```

Register 21.17. HMAC_SOFT_JTAG_CTRL_REG (0x00F8)

![Register 21.17 Bit Diagram](image_description: A bit field diagram for HMAC_SOFT_JTAG_CTRL_REG showing all bits as 'reserved' except the least significant bit labeled "Reset" with value 0, and a note indicating "HMAC_SOFT_JTAG_CTRL".)

```markdown
HMAC_SOFT_JTAG_CTRL Configures whether or not to enable JTAG authentication mode.
O: Disable
1: Enable
(WO)
```

Espressif Systems

680

ESP32-C6 TRM (Version 1.1)

Submit Documentation Feedback
```