

```markdown
Chapter 10 Reset and Clock

Register 10.57. HP_SYS_CLKRST_HPCORE_WDT_RESET_SOURCEO_REG (0x00EC)

31 2 1 0
+---------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |
+---------------------------------------------+

HP_SYS_CLKRST_HPCOREO_WDT_RESET_SOURCE_SEL Configures the MWDT used to trigger the
HP CPU0 reset.
O: MWDTO
1: MWDT1
(R/W)

HP_SYS_CLKRST_HPCORE1_WDT_RESET_SOURCE_SEL Configures the MWDT used to trigger the
HP CPU1 reset.
O: MWDTO
1: MWDT1
(R/W)
```