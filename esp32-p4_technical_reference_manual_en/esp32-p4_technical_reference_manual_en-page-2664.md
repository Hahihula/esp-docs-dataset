

```markdown
Register 52.30. EMACADDROLOW_REG (0x0044)

EMACADDROLOW_REG Configures the lower 32 bits of the first 6-byte MAC address.
The MAC uses this field for filtering the received frames and inserting the MAC address in the Transmit Flow Control (PAUSE) Frames. (R/W)


Register 52.31. EMACADDR1HIGH_REG (0x004B)

ADDRESS_ENABLE1 Configures whether to enable perfect filtering using the second MAC address.
O: Disable
1: Enable
(R/W)

SOURCE_ADDRESS Configures whether to which fields of the received frame EMACADDR1 [47:0] compares.
O: The DA fields
1: The SA fields
(R/W)

MASK_BYTE_CONTROL Configures whether to mask MAC address byte bytes when comparing the received DA or SA with the contents of EMACADDR1.
O: Unmask
1: Mask

The correspondence between the mask control bits and the bytes:
Bit[29]: EMACADDR1HIGH_REG[15:8]
Bit[28]: EMACADDR1HIGH_REG[7:0]
Bit[27]: EMACADDR1LOW_REG[31:24]
Bit[24]: EMACADDR1LOW_REG[7:0]

You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address.(R/W)

MAC_ADDRESS1_HI Configures the upper 16 bits of the second 6-byte MAC address [47:32]. (R/W)
```