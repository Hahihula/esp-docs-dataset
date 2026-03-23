

```markdown
Chapter 23 External Memory Encryption and Decryption (XTS_AES) GoBack


Register 23.7. XTS_AES_DESTROY_REG (0x0054)

XTS_AES_DESTROY
(eserved)
31 | 1 | 0
-------------------------------------------------
| OxoOOOOOOO | x Reset

XTS_AES_DESTROY Write 1 to destroy encrypted result. (WO)


Register 23.8. XTS_AES_STATE_REG (0x0058)

XTS_AES_STATE
(eserved)
31 | 2 | 1 | 0
-------------------------------------------------
| OxoOOOOOOO | OxO Reset

XTS_AES_STATE Indicates the status of the Manual Encryption block.
• 0x0 (XTS_AES_IDLE): idle;
• 0x1 (XTS_AES_BUSY): busy with encryption;
• 0x2 (XTS_AES_DONE): encryption is completed, but the encrypted result is not accessible to SPI;
• 0x3 (XTS_AES_RELEASE): encrypted result is accessible to SPI. (RO)


Register 23.9. XTS_AES_DATE_REG (0x005C)

XTS_AES_DATE
(eserved)
31 | 30 | 29 | 0
-------------------------------------------------
| O | O | Ox2O2OO111 Reset

XTS_AES_DATE Version control register. (R/W)


Espressif Systems
543
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```