

```markdown
Register 31.3. TWAI_BUS_TIMING_1_REG (0x001C)

TWAI_TIME_SEG1 The width of PBS1. (RO | R/W)
TWAI_TIME_SEG2 The width of PBS2. (RO | R/W)
TWAI_TIME_SAMP The number of sample points. 0: the bus is sampled once; 1: the bus is sampled three times (RO | R/W)

Register 31.4. TWAI_ERR_WARNING_LIMIT_REG (0x0034)

TWAI_ERR_WARNING_LIMIT Error warning threshold. In the case when any of an error counter value exceeds the threshold, or all the error counter values are below the threshold, an error warning interrupt will be triggered (given the enable signal is valid). (RO | R/W)
```