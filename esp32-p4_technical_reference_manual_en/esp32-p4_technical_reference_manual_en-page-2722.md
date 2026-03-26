

```markdown
Register 53.17. TWAI_INTERRUPT_REG (0x000C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 9   | TWAI_IDLE_INT_ST                                                             |
| 8   | TWAI_BUS_ERR_INT_ST                                                         |
| 7   | TWAI_ARBITRATION_LOST_INT_ST                                                |
| 6   | TWAI_ERR_PASSIVE_INT_ST                                                     |
| 5   | TWAI_ERR_WARNING_INT_ST                                                     |
| 4   | TWAI_DATA_OVERRUN_INT_ST                                                    |
| 3   | TWAI_TS_COUNTER_OVFL_INT_ST                                                 |
| 2   | TWAI_TRANSMIT_INT_ST                                                         |
| 1   | TWAI_RECEIVE_INT_ST                                                          |
| 0   | Reset                                                                       |

TWAI_RECEIVE_INT_ST The masked interrupt status of TWAI_RX_INT. (RO)
TWAI_TRANSMIT_INT_ST The masked interrupt status of TWAI_TX_INT. (RO)
TWAI_ERR_WARNING_INT_ST The masked interrupt status of TWAI_ERR_WARN_INT. (RO)
TWAI_DATA_OVERRUN_INT_ST The masked interrupt status of TWAI_OVERRUN_INT. (RO)
TWAI_TS_COUNTER_OVFL_INT_ST The masked interrupt status of TWAI_TS_COUNTER_OVFL_INT. (RO)
TWAI_ERR_PASSIVE_INT_ST The masked interrupt status of TWAI_ERR_PASSIVE_INT. (RO)
TWAI_ARBITRATION_LOST_INT_ST The masked interrupt status of TWAI_ARB_LOST_INT. (RO)
TWAI_BUS_ERR_INT_ST The masked interrupt status of TWAI_BUS_ERR_INT. (RO)
TWAI_IDLE_INT_ST The masked interrupt status of TWAI_BUS_STATE_INT. (RO)
```