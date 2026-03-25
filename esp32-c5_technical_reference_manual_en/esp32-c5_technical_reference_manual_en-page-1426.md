

```markdown
Register 38.30. TWAIFD_EWL_ERP_FAULT_STATE_REG (0x002C)

TWAIFD_EW_LIMIT Configures the error warning limit. If the error warning limit is reached, an interrupt can be generated. The error warning limit indicates a heavily disturbed bus. (R/W)

TWAIFD_ERP_LIMIT Configures the error passive limit. When one of the error counters (REC/TEC) exceeds this value, the fault confinement state changes to error-passive. (R/W)

TWAIFD_ERA Represents the fault state of error-active.
0: Not error-active
1: Error-active
(RO)

TWAIFD_ERP Represents the fault state of error-passive.
0: Not error-passive
1: Error-passive
(RO)

TWAIFD_BOF Represents the fault state of bus-off.
0: Not bus-off
1: Bus-off
(RO)
```

```markdown
Register 38.31. TWAIFD_REC_TEC_REG (0x0030)

TWAIFD_REC_VAL Represents the receiver error counter value. (RO)

TWAIFD_TEC_VAL Represents the transmitter error counter value. (RO)
```