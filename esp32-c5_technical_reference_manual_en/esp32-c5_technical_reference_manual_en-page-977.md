

```markdown
Chapter 29 External Memory Encryption and Decryption (XTS_AES) GoBack


Register 29.3. XTS_AES_DESTINATION_REG (0x0344)

[Diagram: Bitfield for register XTS_AES_DESTINATION_REG showing bit 1 as XTS_AES_DESTINATION with reset value 0, bits 31-0 reserved except for this bit.]

XTS_AES_DESTINATION Configures the type of external memory for Manual Encryption. Currently, it must be set to 0, as the Manual Encryption block only supports flash encryption. Set this bit to 1 may cause an error.
O: flash
1: external RAM
(R/W)


Register 29.4. XTS_AES_PHYSICAL_ADDRESS_REG (0x0348)

[Diagram: Bitfield for register XTS_AES_PHYSICAL_ADDRESS_REG showing bits 31-29 reserved, bit values at reset are all 0.]

XTS_AES_PHYSICAL_ADDRESS Configures the physical address which will be used in Manual Encryption. This value should be aligned with the byte number configured via the XTS_AES_LINESIZE parameter. (R/W)
```