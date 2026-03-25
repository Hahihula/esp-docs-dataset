

# 10.5 Registers

The addresses in this section are relative to Event Task Matrix base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 10.1. SOC_ETM_CH_ENA_ADO_REG (0x0000)

```
31    30    29    28    27    26    25    24    23    22    21    20    19    18    17    16    15    14    13    12    11    10    9     8     7     6     5     4     3     2     1     0
+-------------------------------------------------------------------------------------------------------------------------------+
| SOC_ETM_CH_ENABLED31 | SOC_ETM_CH_ENABLED30 | SOC_ETM_CH_ENABLED29 | ... | SOC_ETM_CH_ENABLED4 | SOC_ETM_CH_ENABLED3 | SOC_ETM_CH_ENABLED2 | SOC_ETM_CH_ENABLED1 | SOC_ETM_CH_ENABLED0 |
+-------------------------------------------------------------------------------------------------------------------------------+
| 0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 | Reset
```

SOC_ETM_CH_ENABLEDn (n: 0-31) Represents channeln enable status.

0: Disable  
1: Enable  
(R/WTC/WS)

## Register 10.2. SOC_ETM_CH_ENA_AD1_REG (0x000C)

```
31    30    29    28    27    26    25    24    23    22    21    20    19    18    17    16    15    14    13    12    11    10    9     8     7     6     5     4     3     2     1     0
+-------------------------------------------------------------------------------------------------------------------------------+
| (reserved) | SOC_ETM_CH_ENABLED49 | SOC_ETM_CH_ENABLED48 | ... | SOC_ETM_CH_ENABLED34 | SOC_ETM_CH_ENABLED33 | SOC_ETM_CH_ENABLED32 |
+-------------------------------------------------------------------------------------------------------------------------------+
| 0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 | Reset
```

SOC_ETM_CH_ENABLEDn (n: 32-49) Represents channeln enable status.

0: Disable  
1: Enable  
(R/WTC/WS)