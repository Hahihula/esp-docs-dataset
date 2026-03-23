

```markdown
Table 4.3-2 lists all key purpose and their values. Setting the eFuse parameter `EFUSE_KEY_PURPOSE_n` declares the purpose of KEYn (n: 0 ~ 5).

Table 4.3-2. Secure Key Purpose Values

| Key Purpose Values | Purposes |
|--------------------|----------|
| 0                  | User purposes |
| 1                  | Reserved |
| 2                  | Reserved |
| 3                  | Reserved |
| 4                  | XTS_AES_128_KEY (flash/SRAM encryption and decryption) |
| 5                  | HMAC Downstream mode (both JTAG and DS) |
| 6                  | JTAG in HMAC Downstream mode |
| 7                  | Digital Signature peripheral in HMAC Downstream mode |
| 8                  | HMAC Upstream mode |
| 9                  | SECURE_BOOT_DIGEST0 (secure boot key digest) |
| 10                 | SECURE_BOOT_DIGEST1 (secure boot key digest) |
| 11                 | SECURE_BOOT_DIGEST2 (secure boot key digest) |

Table 4.3-3 provides the details of parameters in BLOCK1 ~ BLOCK10.
```