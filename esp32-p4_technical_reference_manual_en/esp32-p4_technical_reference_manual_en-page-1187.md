

```markdown
Register 19.62. PMS_COREn_MM_HP_PERI_PMS_REG1_REG (n: 0–1) (0x000C+0x20*n)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0   | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | Reset |

PMS_COREn_MM_HP_USBOTG_ALLOW Configures whether HP CPU in machine mode has permission to access HP high-speed USB 2.0 OTG.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_MM_HP_USBOTG11_ALLOW Configures whether HP CPU in machine mode has permission to access HP full-speed USB 2.0 OTG.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_MM_HP_USBOTG11_WRAP_ALLOW Configures whether HP CPU in machine mode has permission to access HP full-speed USB 2.0 OTG's wrap.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_MM_HP_GDMA_ALLOW Configures whether HP CPU in machine mode has permission to access HP VDMA.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_MM_HP_SDMMC_ALLOW Configures whether HP CPU in machine mode has permission to access HP SDMMC.
O: Not allowed
1: Allowed
(R/W)
```