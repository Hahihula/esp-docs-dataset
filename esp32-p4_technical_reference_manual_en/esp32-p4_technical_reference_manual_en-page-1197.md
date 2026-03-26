

```markdown
Register 19.65. PMS_COREn_UM_HP_PERI_PMS_REGO_REG (n: 0-1) (0x0018+0x20*n)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| (reserved) | PMS_COREn_UM_CACHE_ALLOW | PMS_COREn_UM_MON_ALLOW | PMS_COREn_UM_SPM_ALLOW | PMS_COREn_UM_L2MEM_ALLOW | PMS_COREn_UM_CPU_ALLOW | PMS_COREn_UM_TRACEn_ALLOW | (reserved) | PMS_COREn_UM_L2ROM_ALLOW | PMS_COREn_UM_FLASH_ALLOW | PMS_COREn_UM_PSRAAllow |
| Reset | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 |

PMS_COREn_UM_PSRAAllow Configures whether HP CPU in user mode has permission to access external RAM without going through cache.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_FLASH_ALLOW Configures whether HP CPU in user mode has permission to access external flash without going through cache.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_L2MEM_ALLOW Configures whether HP CPU in user mode has permission to access HP L2MEM without going through cache.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_L2ROM_ALLOW Configures whether HP CPU in user mode has permission to access HP ROM without going through cache.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_TRACE0_ALLOW Configures whether HP CPU in user mode has permission to access TRACE0.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_TRACE1_ALLOW Configures whether HP CPU in user mode has permission to access TRACE1.
O: Not allowed
1: Allowed
(R/W)
```
Continued on the next page...
```