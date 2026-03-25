

# 25.7 Registers

The addresses in this section are relative to the RSA accelerator base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 25.1. RSA_M_PRIME_REG (0x0800)

```
31                                 0
+----------------------------------------------------------+
|                0x000000               | Reset
+----------------------------------------------------------+
```

**RSA_M_PRIME** Configures M'.  
(R/W)

## Register 25.2. RSA_MODE_REG (0x0804)

```
31                                 7   6           0
+-----------------------------------------------+
| (reserved) ... | RSA_MODE | Reset
+-----------------------------------------------+
```

**RSA_MODE** Configures the RSA length.  
(R/W)

## Register 25.3. RSA_SET_START_MODEXP_REG (0x080C)

```
31                                 1   0
+-----------------------------+
|               Reset        |
+-----------------------------+
```

**RSA_SET_START_MODEXP** Configures whether or not to start the modular exponentiation.

- 0: No effect  
- 1: Start  
(WT)