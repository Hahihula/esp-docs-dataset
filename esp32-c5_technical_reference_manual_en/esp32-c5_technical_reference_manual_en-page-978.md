

```markdown
Chapter 29 External Memory Encryption and Decryption (XTS_AES) GoBack

Register 29.5. XTS_AES_DPA_CTRL_REG (0x0388)

| Bit | Description          |
|-----|----------------------|
| 31  | (reserved)           |
| 5-4 | 0x0                  |
| 3-2 | 0x1                  |
| ... | ...                  |
| 0   | Reset                |

XTS_AES_CRYPT_DPA_SELECT_REGISTER Configures whether the clock Anti-DPA function is controlled by eFuse or register.  
O: The clock Anti-DPA function is configured by register.  
1: The clock Anti-DPA function is configured by eFuse.  
(R/W)

XTS_AES_CRYPT_CALC_D_DPA_EN Configures whether to enable the clock Anti-DPA in the XTS_AES algorithm.  
O: Enable the clock Anti-DPA only when calculating Tweak value  
1: Enable the clock Anti-DPA both when calculating Tweak value and Date units  
Note that this field is only effective when XTS_AES_CRYPT_SECURITY_LEVEL is not 0.  
(R/W)

XTS_AES_CRYPT_SECURITY_LEVEL Configures the security level of external memory encryption and decryption.  
O: Disable the clock Anti-DPA function  
1-7: The bigger the number is, the more secure the encryption and decryption are  
(R/W)
```