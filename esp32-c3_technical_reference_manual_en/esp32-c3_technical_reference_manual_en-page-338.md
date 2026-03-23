

# 14.10 Registers

The addresses in this section are relative to the Permission Control base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 14.1. PMS_PRIVILEGE_MODE_SEL_LOCK_REG (0x0008)

```
31
+---------------------------------------------+
|                                         |
|  (reserved)                               |
|                                         |
+---------------------------------------------+
| Reset                                     |
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 |
+---------------------------------------------+
```

PMS_PRIVILEGE_MODE_SEL_LOCK Set this bit to lock privilege_mode configuration register. (R/WL)