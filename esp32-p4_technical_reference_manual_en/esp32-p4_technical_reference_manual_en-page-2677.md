

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC)

Register 52.51. EMACSUB2NDINCR_REG (0x0704)
```
31 | (reserved) | SSINC | 8 | 7 | 0
---|------------|-------|----|----|----
0 | 0 | 0 | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x00 Reset

SSINC Configures the value accumulated every clock cycle (PTP clock) with the contents of the sub-second register.
For example, when PTP clock is 50 MHz (the period is 20 ns), you should program 20 (0x14) when the System Time-Nanoseconds register has an accuracy of 1 ns (EMACTSTPCTRL_REG[9], i.e., the TSCTRLSSR bit is set). When TSCTRLSSR is cleared, the Nanoseconds register has a resolution of 0.465 ns. In this case, you should program a value of 43 (0x2B) that is derived by 20 ns/0.465. (R/W)

Register 52.52. EMACSYSSTIM2ND_REG (0x0708)
```
31 | 0
---|----
| 0x00000000 Reset

TSS Represents the current value of the System Time maintained by the MAC.
Measurement unit: second. (RO)

Register 52.53. EMACSYSSTIMNS_REG (0x070C)
```
31 | TSSS
---|------
reserved) | 30 | 0
---|----
0 | 0x00000000 Reset

TSSS Represents the sub-second representation of time, with an accuracy of 0.46 ns.
When EMACTSTPCTRL_REG[9] (TSCTRLSSR) is set, each bit represents 1 ns and the maximum value is 0x3B9A_C9FF. (RO)

Register 52.54. EMAC2NDUPT_REG (0x0710)
```
31 | 0
---|----
| 0x00000000 Reset

TSSSUPD Configures the time to be initialized or added to the system time.
Measurement unit: second. (R/W)

Espressif Systems
2677
ESP32-P4 TRM
PRELIMINARY
```