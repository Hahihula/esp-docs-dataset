

```markdown
Table 5.3-2 lists all key purposes and their values. Set EFUSE_KEY_PURPOSE_n to declare the purpose of KEYn (n: 0 ~ 5).

Table 5.3-2. Secure Key Purpose Values

| Key Purpose Values | Purposes                                                                 |
|--------------------|--------------------------------------------------------------------------|
| 0                  | User purposes                                                            |
| 1                  | ECDSA_KEY                                                                |
| 2                  | Reserved                                                                 |
| 3                  | Reserved                                                                 |
| 4                  | XTS_AES_128_KEY (flash/SRAM encryption and decryption)                   |
| 5                  | HMAC Downstream mode (both JTAG and DSA)                                 |
| 6                  | JTAG in HMAC Downstream mode                                             |
| 7                  | Digital Signature Algorithm peripheral in HMAC Downstream mode           |
| 8                  | HMAC Upstream mode                                                       |
| 9                  | SECURE_BOOT_DIGEST0 (secure boot key digest)                             |
| 10                 | SECURE_BOOT_DIGEST1 (secure boot key digest)                             |
| 11                 | SECURE_BOOT_DIGEST2 (secure boot key digest)                             |

Table 5.3-3 provides the details of parameters in BLOCK1 ~ BLOCK10.
```