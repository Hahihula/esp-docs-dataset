

```markdown
Chapter 34 Key Manager

Register 34.5. HUK_INT_CLR_REG (0x0014)

HUK_PREP_DONE_INT_CLR Write 1 to clear the HUK_PREP_DONE_INT interrupt.
(WT)

HUK_PROC_DONE_INT_CLR Write 1 to clear the HUK_PROC_DONE_INT interrupt.
(WT)

HUK_POST_DONE_INT_CLR Write 1 to clear the HUK_POST_DONE_INT interrupt.
(WT)

Register 34.6. HUK_CONF_REG (0x0020)

HUK_MODE Configures HUK mode.
O: HUK Recovery Mode
1: HUK Generation Mode
(R/W)

Register 34.7. HUK_START_REG (0x0024)

HUK_START Write 1 to start HUK Generator at IDLE phase.
(WT)

HUK_CONTINUE Write 1 to continue HUK Generator operation at LOAD/GAIN phase.
(WT)
```