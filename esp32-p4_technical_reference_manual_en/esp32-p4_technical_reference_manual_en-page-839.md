

# 13.5 Registers

The addresses in this section are relative to Event Task Matrix base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 13.1. SOC_ETM_CH_ENA_ADO_REG (0x0000)

```
31    30    29    28    27    26    25    24    23    22    21    20    19    18    17    16    15    14    13    12    11    10    9    8    7    6    5    4    3    2    1    0
+-----------------------------------------------------------------------------------------------------------------------------+
| SOC_ETM_CH_ENABLED31 | SOC_ETM_CH_ENABLED30 | SOC_ETM_CH_ENABLED29 | ... | SOC_ETM_CH_ENABLED4 | SOC_ETM_CH_ENABLED3 | SOC_ETM_CH_ENABLED2 | SOC_ETM_CH_ENABLED1 | SOC_ETM_CH_ENABLED0 |
+-----------------------------------------------------------------------------------------------------------------------------+
| 0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0 | Reset |
+-----------------------------------------------------------------------------------------------------------------------------+
```

**SOC_ETM_CH_ENABLEDn (n: 0-31)** Represents the status of channeln.

- 0: Disabled
- 1: Enabled  
(R/WTC/SS)

## Register 13.2. SOC_ETM_CH_ENA_AD1_REG (0x000C)

```
31    30    29    28    27    26    25    24    23    22    21    20    19    18    17    16    15    14    13    12    11    10    9    8    7    6    5    4    3    2    1    0
+-----------------------------------------------------------------------------------------------------------------------------+
| (reserved) | SOC_ETM_CH_ENABLED49 | SOC_ETM_CH_ENABLED48 | ... | SOC_ETM_CH_ENABLED34 | SOC_ETM_CH_ENABLED33 |
+-----------------------------------------------------------------------------------------------------------------------------+
| 0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0 | Reset |
+-----------------------------------------------------------------------------------------------------------------------------+
```

**SOC_ETM_CH_ENABLEDn (n: 32-49)** Represents the status of channeln.

- 0: Disabled
- 1: Enabled  
(R/WTC/SS)