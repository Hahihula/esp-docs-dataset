

```markdown
| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | PMS_HP_CORE1_MM_REGION_PMS                                                 |
| 29  | PMS_HP_COREO_MM_REGION_PMS                                                 |
| 28  | PMS_HP_COREO_UM_REGION_PMS                                                 |
| 27  | PMS_LP_CORE_REGION_PMS                                                     |
| 3   | Reset                                                                      |
```

PMS_LP_CORE_REGION_PMS Configures whether LP core in machine mode has permission to access address region0 and address region1. Bit0 corresponds to region0 and bit1 corresponds to region1.
- O: Not allowed
- 1: Allowed
(R/W)

PMS_HP_COREO_UM_REGION_PMS Configures whether HP CPU0 in user mode has permission to access address region0 and address region1. Bit2 corresponds to region0 and bit3 corresponds to region1.
- O: Not allowed
- 1: Allowed
(R/W)

PMS_HP_COREO_MM_REGION_PMS Configures whether HP CPU0 in machine mode has permission to access address region0 and address region1. Bit4 corresponds to region0 and bit5 corresponds to region1.
- O: Not allowed
- 1: Allowed
(R/W)

PMS_HP_CORE1_UM_REGION_PMS Configures whether HP CPU1 in user mode has permission to access address region0 and address region1. Bit6 corresponds to region0 and bit7 corresponds to region1.
- O: Not allowed
- 1: Allowed
(R/W)

PMS_HP_CORE1_MM_REGION_PMS Configures whether HP CPU1 in machine mode has permission to access address region0 and address region1. Bit8 corresponds to region0 and bit9 corresponds to region1.
- O: Not allowed
- 1: Allowed
(R/W)
```