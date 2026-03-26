

```markdown
Register 23.2. LP_ANA_VDD_SOURCE_CNTL_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 2  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | LP_ANA_VGOOD_EVENT_RECORD | LP_ANA_VBAT_EVENT_RECORD_CLR | LP_ANA_BOD_SOURCE_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | LP_ANA_VGOOD_EVENT_RECORD | (reserved) | LP_ANA_VBAT_EVENT_RECORD_CLR |

LP_ANA_VGOOD_EVENT_RECORD Flags for indicating pins whose voltage is lower than the threshold.
O: Under-voltage does not happen on either VDD_BAT or VDD_ANA;
1: Under-voltage happens on VDD_BAT;
2: Under-voltage happens on VDD_ANA;
3: Under-voltage happens on both VDD_BAT and VDD_ANA.
(RO)

LP_ANA_VBAT_EVENT_RECORD_CLR Clear the flags.
O: Not clear
1: Clear the brown-out flag of VDD_BAT
2: Clear the brown-out flag of VDD_ANA
3: No effect
(WT)

LP_ANA_BOD_SOURCE_ENA Configure to detect monitoring sources.
O: Not detecting any pins;
1: Only detect VDD_BAT;
2: Only detect VDD_ANA;
3: Detect both VDD_BAT and VDD_ANA.
(R/W)
```