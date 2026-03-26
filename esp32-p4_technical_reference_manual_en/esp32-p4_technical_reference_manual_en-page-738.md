

```markdown
|31|17|16|9|8|1|0|
|:----|:----|:----|:----|:----|:----|:----|
|| || | | ||
|0| | | | | |Reset|

HP_SYS_CLKRST_HPCOREO_STALL_EN Configures the behavior when MWDT triggers HP CPUO reset.
0: Immediately reset HP CPUO
1: Stall HP CPUO first (R/W)

HP_SYS_CLKRST_HPCOREO_STALL_WAIT_NUM Configures the duration of HP CPUO stall when MWDT triggers HP CPUO reset and HP_SYS_CLKRST_HPCOREO_STALL_EN is set to 1.
Measurement unit: Clock cycles. (R/W)

HP_SYS_CLKRST_WDT_HPCOREO_RST_LEN Configures the duration of the reset when MWDT triggers HP CPUO reset.
Measurement unit: Clock cycles. (R/W)
```