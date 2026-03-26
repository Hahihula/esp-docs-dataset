

```markdown
Register 52.44. EMACADDR7LOW_REG (0x007C)

31 | 0
+-----------------------------+
| 0xFFFFFFFF                 |
+-----------------------------+

EMACADDR7LOW_REG Configures the lower 32 bits of the eighth 6-byte MAC address.
The content of this field is undefined until loaded by the Application after the initialization process.(R/W)


Register 52.45. EMACADDR8HIGH_REG (0x0080)

ADDRESS_ENABLE8 | SOURCE_ADDRESS8 | MASK_BYTE_CONTROL8 | MAC_ADDRESS8_HI
31 | 30 | 29 | 24 | 23 | 16 | 15 | 0
+-----------------------------+
| 0x00 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0FFF |
+-----------------------------+

ADDRESS_ENABLE8 Configures whether to enable perfect filtering using the ninth MAC address.
O: Disable
1: Enable
(R/W)

SOURCE_ADDRESS8 Configures whether to which fields of the received frame EMACADDR8 [47:0] compares.
O: The DA fields
1: The SA fields
(R/W)

MASK_BYTE_CONTROL8 Configures whether to mask MAC address byte bytes when comparing the received DA or SA with the contents of EMACADDR8.
O: Unmask
1: Mask

The correspondence between the mask control bits and the bytes:
Bit[29]: EMACADDR8HIGH_REG[15:8]
Bit[28]: EMACADDR8HIGH_REG[7:0]
Bit[27]: EMACADDR8LOW_REG[31:24]
Bit[24]: EMACADDR8LOW_REG[7:0]

You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address. (R/W)

MAC_ADDRESS8_HI Configures the upper 16 bits of the ninth 6-byte MAC address [47:32]. (R/W)
```