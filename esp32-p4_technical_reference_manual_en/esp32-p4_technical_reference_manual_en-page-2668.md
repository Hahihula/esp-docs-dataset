
```markdown
Register 52.38. EMACADDR4LOW_REG (0x0064)

EMACADDR4LOW_REG Configures the lower 32 bits of the fifth 6-byte MAC address.
The content of this field is undefined until loaded by the Application after the initialization process. (R/W)


Register 52.39. EMACADDR5HIGH_REG (0x0068)

ADDRESS_ENABLE5 Configures whether to enable perfect filtering using the sixth MAC address.
O: Disable
1: Enable
(R/W)

SOURCE_ADDRESS5 Configures whether to which fields of the received frame EMACADDR5 [47:0] compares.
O: The DA fields
1: The SA fields
(R/W)

MASK_BYTE_CONTROL5 Configures whether to mask MAC address byte bytes when comparing the received DA or SA with the contents of EMACADDR5.
O: Unmask
1: Mask

The correspondence between the mask control bits and the bytes:
Bit[29]: EMACADDR5HIGH_REG[15:8]
Bit[28]: EMACADDR5HIGH_REG[7:0]
Bit[27]: EMACADDR5LOW_REG[31:24]
Bit[24]: EMACADDR5LOW_REG[7:0]

You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address. (R/W)

MAC_ADDRESS5_HI Configures the upper 16 bits of the sixth 6-byte MAC address [47:32]. (R/W)
```