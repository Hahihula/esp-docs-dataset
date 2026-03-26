

# 28.7 Registers

The addresses in this section are relative to the RSA accelerator base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section IX .

Register 28.1. RSA_M_PRIME_REG (0x0800)

```
31                                 0
+-------------------------------------+
|        0x000000         |
+-------------------------------------+
Reset
```

RSA_M_PRIME Represents M'. (R/W)

Register 28.2. RSA_MODE_REG (0x0804)

```
31                                 6   0
+-----------------------------+-----------------+
| (reserved)                 |       RSA_MODE    |
+-----------------------------+-----------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
+-----------------------------------------------------+
```

RSA_MODE Configures the RSA length. (R/W)

Register 28.3. RSA_SET_START_MODEXP_REG (0x080C)

```
31                                 1   0
+---------------------------------------+
|        0x000000         |
+---------------------------------------+
Reset
```

RSA_SET_START_MODEXP Configures whether or not to starts the modular exponentiation.

O: No effect  
1: Start  
(WT)