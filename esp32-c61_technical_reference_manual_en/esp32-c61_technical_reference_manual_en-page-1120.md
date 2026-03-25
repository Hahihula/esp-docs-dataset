

# 30.9 Registers

The addresses in this section are relative to the SDIO Slave Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

## 30.9.1 HINF Registers

Register 30.1. HINF_CFG_DATAO_REG (0x0000)

```
31                                 16                 15                  0
+--------------------------------------------------------------------------------------------------+
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
|                                                                                                    |
+--------------------------------------------------------------------------------------------------+
0x92                                 0x6666             Reset
```

HINF_DEVICE_ID_FN1 Configures device ID of function 1 in SDIO CIS. (R/W)

HINF_USER_ID_FN1 Configures user ID of function 1 in SDIO CIS. (R/W)