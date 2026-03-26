

```markdown
Register 20.78. HP_SYSTEM_ICM_CPU_ADDRHOLE_INFO_REG (0x0044)

31                                 10                                  9                 8                7                  5               4                    0
+-------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | Reset |
+-------------------------------------------------------------------------------------------------+

HP_SYSTEM_ICM_CPU_ADDRHOLE_ID    Records the master ID when ICM_CPU_ADDRHOLE_INT occurs.
0: HP CPU0
1: HP CPU1
2: LP CPU
3: USBOTGFS
5: GMAC
6: SDMMC
7: USBOTGHS
8: TRACEO
9: TRACE1
10: SPM Monitor
11: L2MEM Monitor
16-31: AHB GDMA (RO)

HP_SYSTEM_ICM_CPU_ADDRHOLE_WR    Records the type of transfer when ICM_CPU_ADDRHOLE_INT occurs.
0: Read transfer
1: Write transfer (RO)

HP_SYSTEM_ICM_CPU_ADDRHOLE_SECURE  Records the type of access error when ICM_CPU_ADDRHOLE_INT occurs.
0: Unauthorized access
1: Illegal access (RO)
```