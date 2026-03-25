

```markdown
* 0: only the primary comparator matches, and the secondary comparator has no effect
* 1: both the primary comparator and the secondary comparator match (P&S)
* 2: neither the primary comparator nor secondary comparator match !(P&S)
* 3: start filtering when primary matches up until secondary matches

If TRACE_P_NOTIFY or TRACE_S_NOTIFY is set, the comparator will report the matched address as a notification, the instructions will not be filtered. For example:

- If the TRACE_MATCH_MODE is 0, and TRACE_P_NOTIFY is set, then all instructions will be traced, and the matched primary comparator will be notified. For details about notify, please refer to Section 3.8.5.
- If the TRACE_MATCH_MODE is 0, and TRACE_S_NOTIFY is set, the instruction will be filtered by the primary comparator, and the instruction that matches the secondary comparator will be notified.

2. Set TRACE_FILTER_EN to enable filter unit.

### 3.8.3 Enable Encoder

* Configure the address space for the trace memory via `TRACE_MEM_START_ADDR_REG` and `TRACE_MEM_END_ADDR_REG`. The encoder can access `0x40800000 ~ 0x4085FFFF`
* Update the value of `TRACE_MEM_CURRENT_ADDR_REG` to the value of `TRACE_MEM_START_ADDR_REG` by setting `TRACE_MEM_CURRENT_ADDR_UPDATE`
* (Optional) Configure the memory writing mode via the `TRACE_MEM_LOOP` bit of `TRACE_TRIGGER_REG`

    - 0: Non-loop mode
    - 1: Loop mode (default)

* Configure the synchronization mode via the `TRACE_RESYNC_MODE` bit of `TRACE_RESYNC_PROLONGED_REG`

    - 0: Disable the synchronization counter
    - 1: Invalid. No effect
    - 2: Synchronization counter counts by packet
    - 3: Synchronization counter counts by cycle

* (Optional) Configures the threshold for the synchronization counter (default value is 128) via `TRACE_RESYNC_PROLONGED_REG`

* (Optional) Enable Interrupt

    - Set the corresponding bit of `TRACE_INTR_ENA_REG` to enable the corresponding interrupt
    - Set the corresponding bit of `TRACE_INTR_CLR_REG` to clear the corresponding interrupt
    - Read `TRACE_INTR_RAW_REG` to know which interrupt occurs

* (Optional) Enable automatic restart by setting the `TRACE_RESTART_ENA` bit of `TRACE_TRIGGER_REG`. This function is enabled by default
```