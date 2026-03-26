

# 29.7 Registers

The addresses in this section are relative to SHA accelerator base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 29.1. SHA_MODE_REG (0x0000)

SHA_MODE Configures the SHA algorithm.
```
0: SHA-1
1: SHA-224
2: SHA-256
3: SHA-384
4: SHA-512
5: SHA-512/224
6: SHA-512/256
7: SHA-512/t
(R/W)
```

## Register 29.2. SHA_T_STRING_REG (0x0004)

SHA_T_STRING Configures t_string for calculating the initial Hash value for SHA-512/t. (R/W)

## Register 29.3. SHA_T_LENGTH_REG (0x0008)

SHA_T_LENGTH Configures t_length for calculating the initial Hash value for SHA-512/t. (R/W)