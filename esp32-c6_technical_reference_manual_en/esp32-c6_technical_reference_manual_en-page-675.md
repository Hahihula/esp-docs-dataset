

# Chapter 21 HMAC Accelerator (HMAC)

## 21.5 Registers

The addresses in this section are relative to HMAC Accelerator base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 21.1. HMAC_SET_START_REG (0x0040)

```
HMAC_SET_START Configures whether or not to enable HMAC.
    0: Disable HMAC
    1: Enable HMAC
(WO)
```

### Register 21.2. HMAC_SET_PARA_FINISH_REG (0x004C)

```
HMAC_SET_PARA_END Configures whether to finish HMAC configuration.
    0: No effect
    1: Finish configuration
(WO)
```

### Register 21.3. HMAC_SET_MESSAGE_CALC_BLOCK_REG (0x0050)

```
HMAC_SET_TEXT_ONE Calls SHA to calculate one message block. (WO)
```