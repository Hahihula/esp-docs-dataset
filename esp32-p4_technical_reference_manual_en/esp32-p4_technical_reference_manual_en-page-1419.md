

```markdown
|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|:-----------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
||0x3ff|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
||Reset|

LP_ANA_VDDBAT_CHARGE_UNDERVEROLTAGE_FLAG  Flag indicating that VDD_BAT is charging. (RO)

LP_ANA_VDDBAT_CHARGE_CNT_CLR  Clear the brown-out counter of VDD_BAT. (WT)

LP_ANA_VDDBAT_CHARGE_UPVOLTAGE_TARGET  Configure the voltage-recovery threshold for the brown-out counter of VDD_BAT. When the counter decreases to this threshold, LP_ANA_VDDBAT_CHARGE_UNDERVEROLTAGE_FLAG is cleared to 0. (R/W)

LP_ANA_VDDBAT_CHARGE_UNDERVEROLTAGE_TARGET  Configure the brown-out threshold for the brown-out counter of VDD_BAT. When the counter increases to this threshold, LP_ANA_VDDBAT_CHARGE_UNDERVEROLTAGE_FLAG is set to 1. (R/W)
```