

# 31.8 Registers

The addresses in this section are relative to the ECDSA_DS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 31.1. ECDSA_CONF_REG (0x0004)

```
31
+---------------------------------------------------------------+
| 6   5   4   3   2   1   0 |
| (reserved) ECDSA_ECC_CURVE ECDSA_SOFTWARE_SET_Z (reserved)     |
+---------------------------------------------------------------+
Reset
```

**ECDSA_ECC_CURVE** Configures the elliptic curve used.
- 0: P-192
- 1: P-256
- 2: P-384
- 3: Invalid
(R/W)

**ECDSA_SOFTWARE_SET_Z** Configures how the parameter z is set.
- 0: Generated from SHA result
- 1: Written by software
(R/W)

## Register 31.2. ECDSA_START_REG (0x001C)

```
31
+-----------------------------+
|   2    1    0 |
| (reserved) ECDSA_START ECDSA_LOAD_DONE |
+-----------------------------+
Reset
```

**ECDSA_START** Configures whether to start the ECDSA_DS operation. This bit will be self-cleared after configuration.
- 0: No effect
- 1: Start the ECDSA_DS operation
(WT)

**ECDSA_LOAD_DONE** Write 1 to generate a signal indicating the ECDSA_DS’s LOAD operation is done. This bit will be self-cleared after configuration. (WT)