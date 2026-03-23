

# 22.6 Registers

The addresses in this section are relative to the RSA accelerator base address provided in Table 5.3-2 in Chapter 5 System and Memory.

## Register 22.1. RSA_M_PRIME_REG (0x0800)

```
31                                 0
+-------------------------------------+
|         0x000000          | Reset |
+-------------------------------------+
```

**RSA_M_PRIME** Represents M'. (R/W)

## Register 22.2. RSA_MODE_REG (0x0804)

```
31                                 6   0
+-----------------------------+------+------+
| (reserved)                 | 7    | Reset |
+-----------------------------+------+------+
```

**RSA_MODE** Configures the RSA length. (R/W)

## Register 22.3. RSA_SET_START_MODEXP_REG (0x080C)

```
31                                 1   0
+-------------------------------------+
|         0x000000          | Reset |
+-------------------------------------+
```

**RSA_SET_START_MODEXP** Configures whether or not to starts the modular exponentiation.
- 0: No effect
- 1: Start
(WT)