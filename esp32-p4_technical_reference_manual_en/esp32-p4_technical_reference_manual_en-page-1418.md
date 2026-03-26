

```markdown
Chapter 23 Brown-out Detector

Register 23.3. LP_ANA_VDDBAT_BOD_CNTL_REG (0x000C)

| Bit | Description |
|-----|-------------|
| 31  | `LP_ANA_VDDBAT_UNDERVOLTAGE_FLAG` Flag indicating that under-voltage occurs on VDD_BAT. (RO) |
| 22-21 | `reserved` |
| 12  | `LP_ANA_VDDBAT_UPVOLTAGE_TARGET` Configure the voltage-recovery threshold for the brown-out counter of VDD_BAT. When the counter decreases to this threshold, LP_ANA_VDDBAT_UNDERVOLTAGE_FLAG is cleared to 0. (R/W) |
| 11  | `LP_ANA_VDDBAT_CNTL_CLR` Clear the brown-out counter of VDD_BAT. (WT) |
| 10  | `LP_ANA_VDDBAT_UNDERVOLTAGE_TARGET` Configure the brown-out threshold for the brown-out counter of VDD_BAT. When the counter increases to this threshold, LP_ANA_VDDBAT_UNDERVOLTAGE_FLAG is set to 1. (R/W) |
| 9-0 | `reserved` |

LP_ANA_VDDBAT_UNDERVOLTAGE_FLAG Flag indicating that under-voltage occurs on VDD_BAT.
(RO)

LP_ANA_VDDBAT_CNTL_CLR Clear the brown-out counter of VDD_BAT. (WT)

LP_ANA_VDDBAT_UPVOLTAGE_TARGET Configure the voltage-recovery threshold for the brown-out counter of VDD_BAT. When the counter decreases to this threshold, LP_ANA_VDDBAT_UNDERVOLTAGE_FLAG is cleared to 0. (R/W)

LP_ANA_VDDBAT_UNDERVOLTAGE_TARGET Configure the brown-out threshold for the brown-out counter of VDD_BAT. When the counter increases to this threshold, LP_ANA_VDDBAT_UNDERVOLTAGE_FLAG is set to 1. (R/W)
```