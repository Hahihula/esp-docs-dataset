

```markdown
Chapter 26 External Memory Encryption and Decryption (XTS_AES) GoBack


Register 26.3. XTS_AES_DESTINATION_REG (0x0344)

XTS_AES_DESTINATION Configures the type of external memory. Currently, it must be set to 0, as the Manual Encryption block only supports flash encryption. Set this bit to 1 may cause an error.
O: flash
1: external RAM
(R/W)


Register 26.4. XTS_AES_PHYSICAL_ADDRESS_REG (0x0348)

XTS_AES_PHYSICAL_ADDRESS Configures physical address. Note that its value should be within the range between 0x0000_0000 and 0x00FF_FFFF). (R/W)
```