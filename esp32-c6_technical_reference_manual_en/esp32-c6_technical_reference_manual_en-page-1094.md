

```markdown
Register 33.4. TWAI_ERR_WARNING_LIMIT_REG (0x0034)

TWAI_ERR_WARNING_LIMIT Configures error warning threshold. In the case when any of an error counter value exceeds the threshold, or all the error counter values are below the threshold, an error warning interrupt will be triggered. Valid only when the enable signal is 1. (RO | R/W)
```

```markdown
Register 33.5. TWAI_DATA_O_REG (0x0040)

TWAI_TX_BYTE_0 Configures the 0th byte information of the data to be transmitted in Operation mode. (WO)

TWAI_ACCEPTANCE_CODE_O Configures the 0th byte of the filter code in Reset mode. (R/W)
```