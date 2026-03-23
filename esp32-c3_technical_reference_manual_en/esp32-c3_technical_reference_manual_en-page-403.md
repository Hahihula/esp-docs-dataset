

```markdown
Register 14.72. PMS_DATE_REG (0x0FFC)

31      28     27           0
+-----------------------------+
| (reserved)                 |
| 0   0   0   0              | 0x2010200
+-----------------------------+
Reset

PMS_DATE Date register. (R/W)

Register 14.73. SYSCON_EXT_MEM_PMS_LOCK_REG (0x0020)

31      0
+-----------------------------------------------+
| (reserved)                                   |
| 0   0   0   0   0   0   0   0   0   0   0   0 | 1   0
+-----------------------------------------------+
Reset

SYSCON_EXT_MEM_PMS_LOCK Set this bit to lock the permission configuration related to external memory. (R/W)
```