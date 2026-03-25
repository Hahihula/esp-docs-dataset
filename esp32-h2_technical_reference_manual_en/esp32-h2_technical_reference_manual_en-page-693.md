

```markdown
Register 26.5. XTS_AES_DPA_CTRL_REG (0x0388)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            | (reserved)                                                                  |
| 5   | XTS_AES_CRYPT_DPA_SELECT_REGISTER         | Configures whether the Anti-DPA function is controlled by eFuse or register. <br> O: The Anti-DPA function is configured by register. <br> 1: The Anti-DPA function is configured by eFuse. (R/W) |
| 4   | XTS_AES_CRYPT_CALC_D_DPA_EN               | Configures whether to enable Anti-DPA in the XTS_AES algorithm. <br> O: Enable Anti-DPA only when calculating T <br> 1: Enable Anti-DPA both when calculating T and D <br> Note that this field is only effective when XTS_AES_CRYPT_SECURITY_LEVEL is not O. (R/W) |
| 3   |                                            |                                                                             |
| 2   | XTS_AES_CRYPT_SECURITY_LEVEL              | Configures the security level of external memory encryption and decryption. <br> O: Disable the Anti-DPA function <br> 1-7: The bigger the number is, the more secure the encryption and decryption are (R/W) |
| 1   |                                            |                                                                             |
| 0   |                                            |                                                                             |

Reset value: 0x000000
```
```markdown
XTS_AES_CRYPT_DPA_SELECT_REGISTER Configures whether the Anti-DPA function is controlled by eFuse or register.

O: The Anti-DPA function is configured by register.
1: The Anti-DPA function is configured by eFuse.
(R/W)

XTS_AES_CRYPT_CALC_D_DPA_EN Configures whether to enable Anti-DPA in the XTS_AES algorithm.

O: Enable Anti-DPA only when calculating T
1: Enable Anti-DPA both when calculating T and D
Note that this field is only effective when XTS_AES_CRYPT_SECURITY_LEVEL is not O.
(R/W)

XTS_AES_CRYPT_SECURITY_LEVEL Configures the security level of external memory encryption and decryption.

O: Disable the Anti-DPA function
1-7: The bigger the number is, the more secure the encryption and decryption are
(R/W)
```