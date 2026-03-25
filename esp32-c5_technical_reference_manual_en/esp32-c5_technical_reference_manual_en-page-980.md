

```markdown
Register 29.8. XTS_AES_RELEASE_REG (0x0350)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
|     | YTS_AES_RELEASE [1:0] |
| Reset | 0 |

**XTS_AES_RELEASE** Set this bit to release encrypted result to MSPI.  
0: do not release  
1: release  

This action should only be asserted when manual encryption status is 2. After this action, manual encryption status will become 3. (WT)

---

```markdown
Register 29.9. XTS_AES_DESTROY_REG (0x0354)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
|     | XTS_AES_DESTROY [1:0] |
| Reset | 0 |

**XTS_AES_DESTROY** Set this bit to destroy encrypted result.  
0: No effect  
1: Destroy encrypted result  

This action should be asserted only when manual encryption status is 3. After this action, manual encryption status will become 0. (WT)

---

```markdown
Register 29.10. XTS_AES_STATE_REG (0x0358)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
|     | YTS_AES_STATE [2:0] |
| Reset | 0x0 |

**XTS_AES_STATE** Represents the status of the Manual Encryption block.  
0 (XTS_AES_IDLE): Idle  
1 (XTS_AES_BUSY): Busy with encryption  
2 (XTS_AES_DONE): Encryption completed, but the encrypted result is not accessible to MSPI  
3 (XTS_AES_RELEASE): Encrypted result is accessible to MSPI (RO)
```