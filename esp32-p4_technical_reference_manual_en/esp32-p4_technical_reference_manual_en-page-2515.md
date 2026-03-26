

```markdown
Register 47.10. LP_I2S_INT_CLR_REG (0x0018)

31
+-----------------------------------------------------------------------------+
| 6   5   4   3   2   1   0 |
| +-------------------------+ Reset |
| | (reserved)             | |
+-----------------------------------------------------------------------------+

LP_I2S_RX_DONE_INT_CLR    Write 1 to clear the LP_I2S_RX_DONE_INT interrupt. (WT)
LP_I2S_RX_HUNG_INT_CLR    Write 1 to clear the LP_I2S_RX_DONE_INT interrupt. (WT)
LP_I2S_RX_FIFOMEM_UDF_INT_CLR Write 1 to clear the LP_I2S_RX_FIFOMEM_UDF_INT interrupt. (WT)
LP_VAD_DONE_INT_CLR       Write 1 to clear the LP_I2S_VAD_DONE_INT interrupt. (WT)
LP_VAD_RESET_DONE_INT_CLR Write 1 to clear the LP_I2S_VAD_RESET_DONE_INT interrupt. (WT)
LP_I2S_RX_MEM_THRESHOLD_INT_CLR Write 1 to clear the LP_I2S_RX_MEM_THRESHOLD_INT interrupt. (WT)
```