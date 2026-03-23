

```markdown
Register 4.9. GDMA_AHB_TEST_REG (0x0060)

GDMA_AHB_TESTMODE Reserved. (R/W)
GDMA_AHB_TESTADDR Reserved. (R/W)

Register 4.10. GDMA_MISC_CONF_REG (0x0064)

GDMA_AHBM_RST_INTER Write 1 and then 0 to reset the internal AHB FSM. (R/W)

GDMA_ARB_PRI_DIS Configures whether or not to disable the fixed-priority channel arbitration.
O: Enable
1: Disable
(R/W)

GDMA_CLK_EN Configures clock gating.
O: Support clock only when the application writes registers.
1: Always force the clock on for registers.
(R/W)
```