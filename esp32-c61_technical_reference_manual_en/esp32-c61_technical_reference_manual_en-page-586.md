

```markdown
Register 11.88. PMU_LP_INT_ST_REG (0x0170)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | PMU_ACTIVE_SWITCH_SLEEP_START_INT_ST       | The masked interrupt status of PMU_MODEM_SWITCH_ACTIVE_START_INT. (RO)      |
| 29  | PMU_MODEM_SWITCH_SLEEP_START_INT_ST        | The masked interrupt status of PMU_SLEEP_SWITCH_ACTIVE_START_INT. (RO)      |
| 28  | PMU_SLEEP_SWITCH_ACTIVE_END_INT_ST         | The masked interrupt status of PMU_SLEEP_SWITCH_ACTIVE_END_INT. (RO)        |
| 27  | PMU_SLEEP_SWITCH_MODEM_END_INT_ST          | The masked interrupt status of PMU_SLEEP_SWITCH_MODEM_END_INT. (RO)         |
| 26  | PMU_MODEM_SWITCH_SLEEP_END_INT_ST          | The masked interrupt status of PMU_MODEM_SWITCH_SLEEP_END_INT. (RO)         |
| 25  | PMU_ACTIVE_SWITCH_SLEEP_END_INT_ST         | The masked interrupt status of PMU_ACTIVE_SWITCH_SLEEP_END_INT. (RO)        |
| 24  | PMU_MODEM_SWITCH_ACTIVE_START_INT_ST       | The masked interrupt status of PMU_MODEM_SWITCH_ACTIVE_START_INT. (RO)      |
| 23  | PMU_SLEEP_SWITCH_ACTIVE_START_INT_ST       | The masked interrupt status of PMU_SLEEP_SWITCH_ACTIVE_START_INT. (RO)      |
| 22  | PMU_SLEEP_SWITCH_MODEM_START_INT_ST        | The masked interrupt status of PMU_SLEEP_SWITCH_MODEM_START_INT. (RO)       |
| 21  | PMU_MODEM_SWITCH_SLEEP_START_INT_ST        | The masked interrupt status of PMU_MODEM_SWITCH_SLEEP_START_INT. (RO)       |
| 20  | PMU_ACTIVE_SWITCH_SLEEP_START_INT_ST       | The masked interrupt status of PMU_ACTIVE_SWITCH_SLEEP_START_INT. (RO)      |
| ... | ...                                         | ...                                                                           |
| 0   | Reset                                      | 0                                                                             |

PMU_MODEM_SWITCH_ACTIVE_END_INT_ST    The masked interrupt status of PMU_MODEM_SWITCH_ACTIVE_END_INT. (RO)

PMU_SLEEP_SWITCH_ACTIVE_END_INT_ST     The masked interrupt status of PMU_SLEEP_SWITCH_ACTIVE_END_INT. (RO)

PMU_SLEEP_SWITCH_MODEM_END_INT_ST      The masked interrupt status of PMU_SLEEP_SWITCH_MODEM_END_INT. (RO)

PMU_MODEM_SWITCH_SLEEP_END_INT_ST      The masked interrupt status of PMU_MODEM_SWITCH_SLEEP_END_INT. (RO)

PMU_ACTIVE_SWITCH_SLEEP_END_INT_ST     The masked interrupt status of PMU_ACTIVE_SWITCH_SLEEP_END_INT. (RO)

PMU_MODEM_SWITCH_ACTIVE_START_INT_ST   The masked interrupt status of PMU_MODEM_SWITCH_ACTIVE_START_INT. (RO)

PMU_SLEEP_SWITCH_ACTIVE_START_INT_ST   The masked interrupt status of PMU_SLEEP_SWITCH_ACTIVE_START_INT. (RO)

PMU_SLEEP_SWITCH_MODEM_START_INT_ST    The masked interrupt status of PMU_SLEEP_SWITCH_MODEM_START_INT. (RO)

PMU_MODEM_SWITCH_SLEEP_START_INT_ST    The masked interrupt status of PMU_MODEM_SWITCH_SLEEP_START_INT. (RO)

PMU_ACTIVE_SWITCH_SLEEP_START_INT_ST   The masked interrupt status of PMU_ACTIVE_SWITCH_SLEEP_START_INT. (RO)
```