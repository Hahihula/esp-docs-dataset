

# 20.6 Registers

The addresses in this section are relative to the RSA accelerator base address provided in Table 3.3-3 in Chapter 3 System and Memory.

## Register 20.1. RSA_M_PRIME_REG (0x0800)

```
RSA_M_PRIME_REG Stores M' (R/W)
```

```
31                                 0
+----------------------------------------------------------+
| 0x00000000                                         Reset |
+----------------------------------------------------------+
```

## Register 20.2. RSA_MODE_REG (0x0804)

```
RSA_MODE Stores the mode of modular exponentiation. (R/W)
```

```
31                                 7   6
+-----------------------------------------------+
| (reserved)           0 0 0 0 0 0 0 0 RSA_MODE |
+-----------------------------------------------+
```

## Register 20.3. RSA_CLEAN_REG (0x0808)

```
RSA_CLEAN The content of this bit is 1 when memories complete initialization. (RO)
```

```
31                                 0
+-----------------------------+
| (reserved)                 1 Reset |
+-----------------------------+
```