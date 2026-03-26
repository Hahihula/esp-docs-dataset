

# 27.5 Registers

The addresses in this section are relative to HMAC Accelerator base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 27.1. HMAC_SET_START_REG (0x0040)

```
31
+---------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
+---------------------------------------------------------------+
HMAC_SET_START (reserved)
```

**HMAC_SET_START** Configures whether or not to enable HMAC.
- O: Disable HMAC
- 1: Enable HMAC
(WO)

## Register 27.2. HMAC_SET_PARA_FINISH_REG (0x004C)

```
31
+---------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
+---------------------------------------------------------------+
HMAC_SET_PARA_END (reserved)
```

**HMAC_SET_PARA_END** Configures whether to finish HMAC configuration.
- O: No effect
- 1: Finish configuration
(WO)