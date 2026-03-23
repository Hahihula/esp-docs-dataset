

```markdown
Register 25.5. XTS_AES_DPA_CTRL_REG (0x0388)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            |                                                                             |
|     | 0x00000000                                 | Reset                                                                       |
|     | 0x7                                        | Reset                                                                       |

XTS_AES_CRYPT_DPA_SELECT_REGISTER Configures whether the Anti-DPA function is controlled by eFuse or register.
- 0: The Anti-DPA function is configured by the register.
- 1: The Anti-DPA function is configured by eFuse.
(R/W)

XTS_AES_CRYPT_CALC_D_DPA_EN Configures whether to enable Anti-DPA in the XTS_AES algorithm.
- 0: Enable Anti-DPA only when calculating T
- 1: Enable Anti-DPA both when calculating T and D
Note that this field is only effective when XTS_AES_CRYPT_SECURITY_LEVEL is not 0.
(R/W)

XTS_AES_CRYPT_SECURITY_LEVEL Configures the security level of external memory encryption and decryption.
- 0: Disable the Anti-DPA function
- 1-7: The bigger the number is, the more secure the encryption and decryption are
(R/W)
```

Register 25.6. XTS_AES_TRIGGER_REG (0x034C)

```markdown
| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            |                                                                             |
|     | 0x00000000                                 | Reset                                                                       |
|     | x                                         | Reset                                                                       |

XTS_AES_TRIGGER Configures whether or not to enable manual encryption.
- 0: Disable manual encryption
- 1: Enable manual encryption
(WO)
```