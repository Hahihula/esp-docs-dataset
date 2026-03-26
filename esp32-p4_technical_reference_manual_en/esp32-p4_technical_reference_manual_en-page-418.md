

```markdown
2. Configure the number of tokens for TX and RX respectively via DMA2D_OUT_ARB_TOKEN_NUM_CHn and DMA2D_IN_ARB_TOKEN_NUM_CHn.
3. Enable weight arbitration optimization for TX and RX respectively by clearing DMA2D_OUT_ARB_WEIGHT_OPT_DIS_CHn and DMA2D_IN_ARB_WEIGHT_OPT_DIS_CHn.
4. Enable the arbitration for TX and RX respectively via DMA2D_OUT_WEIGHT_EN and DMA2D_IN_WEIGHT_EN.

## 6.7.7 Resetting 2D-DMA While it Runs

When the 2D-DMA is running, namely when it is still processing descriptors, it must be stopped first before being reset fully via HP_SYS_CLKRST_RST_EN_DMA2D or partially (only reset AXI functions) via DMA2D_AXIM_RD_RST and DMA2D_AXIM_WR_RST. The procedures are as follows:

1. Set DMA2D_IN_CMD_DISABLE_CHn and DMA2D_OUT_CMD_DISABLE_CHn to stop the 2D-DMA.
2. Reset the 2D-DMA when DMA2D_OUT_RESET_AVAIL_CHn and DMA2D_IN_RESET_AVAIL_CHn turn to 1.
3. Clear DMA2D_IN_CMD_DISABLE_CHn and DMA2D_OUT_CMD_DISABLE_CHn to 0 after the 2D-DMA is reset.
```