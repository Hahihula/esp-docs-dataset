

# 24.6 Registers

The addresses in this section are relative to Random Number Generator base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 24.1. LPPERI_RNG_CFG_REG (0x0024)

```
31                                 12   11    10     9                    1                     0
+--------------------------------------------------------------------------------------------------+
| (reserved) | LPPERI_RTC_TIMER_EN | (reserved) | LPPERI_RNG_SAMPLE_ENABLE |
+--------------------------------------------------------------------------------------------------+
| 0 0 0 ... 0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 0 0 0 0 0 0 | Reset
```

**LPPERI_RNG_SAMPLE_ENABLE** Configures whether to enable BUF_CHAIN.  
- 0: Disable  
- 1: Enable  
(R/W)

**LPPERI_RTC_TIMER_EN** Configures whether to enable the RTC timer before CRC.  
- 0: Disable  
- 1: Enable  
(R/W)

**LPPERI_RNG_SAMPLE_CNT** Represents the count value of BUF_CHAIN. (RO)

## Register 24.2. LPPERI_RNG_DATA_SYNC_REG (0x0028)

```
31                                 0
+---------------------------------------------------------------+
| LPPERI_RND_SYNC_DATA |
+---------------------------------------------------------------+
| 0 0 ... 0 | Reset
```

**LPPERI_RND_SYNC_DATA** Represents the RNG synchronization result. (RO)