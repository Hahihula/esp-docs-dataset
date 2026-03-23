

```markdown
Register 9.12. RTC_CNTL_RESET_STATE_REG (0x0038)

RTC_CNTL_RESET_CAUSE_PROCPU Stores the CPU reset cause. (RO)

RTC_CNTL_STAT_VECTOR_SEL_PROCPU Selects the CPU static vector. (R/W)

RTC_CNTL_ALL_RESET_FLAG_PROCPU Indicates the CPU reset flag. (RO)

RTC_CNTL_ALL_RESET_FLAG_CLR_PROCPU Clears the CPU reset flag. (WO)

RTC_CNTL_OCD_HALT_ON_RESET_PROCPU Set this bit to send CPU into halt state upon CPU reset. (R/W)

RTC_CNTL_JTAG_RESET_FLAG_PROCPU Indicates the JTAG reset flag. (RO)

RTC_CNTL_JTAG_RESET_FLAG_CLR_PROCPU Sets the JTAG reset flag. (WO)

RTC_CNTL_DRESET_MASK_PROCPU Set this bit to bybass D-reset. (R/W)


Register 9.13. RTC_CNTL_WAKEUP_STATE_REG (0x003C)

RTC_CNTL_WAKEUP_ENA Selects the wakeup source. For details, please refer to Table 9.4-2. (R/W)
```