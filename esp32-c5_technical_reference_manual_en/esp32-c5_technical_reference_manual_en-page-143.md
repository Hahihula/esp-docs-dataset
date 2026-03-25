

```markdown
- Stop tracing when the CPU is in reset

The encoder will be reset separately, if `TRACE_RESET_ENA` is set. When the CPU is in reset, the encoder will output a packet to report the address of the last instruction before reset, followed by a support packet to indicate that tracing has stopped. Once the CPU exits from reset, the encoder will start tracing again, commencing with a synchronization packet.

- Using trigger outputs from the Debug Module

The debug module of the HP CPU has a trigger unit. This defines a match control register (`mcontrol`) containing a 4-bit `action` field, and reserves codes 2 ~ 4 of this field for trace use. ESP32-C5 has implemented this feature. The values of the `action` field are listed in Table 3.8-1.

Table 3.8-1. Debug module trigger support (the `action` field of the `mcontrol` register)

| Value | Description                     |
|-------|----------------------------------|
| 2     | Trace-on: start trace            |
| 3     | Trace-off: end trace             |
| 4     | Trace-notify: notify the encoder to report an address |

For details about the debug module trigger unit, please refer to Chapter 2 High-Performance CPU.

## 3.8.2 Filter Configuration

The filter unit described in Section 3.5.4 can be configured as follows:

1. Select one of the following match modes:

    - Set `TRACE_MATCH_PRIVILEGE` to enable privilege match mode:
        - Configure `TRACE_MATCH_CHOICE_PRIVILEGE` to specify the privilege level.

    - Set `TRACE_MATCH_ECAUSE` to enable ecause match mode:
        - Configure `TRACE_MATCH_CHOICE_ECAUSE` to specify the ecause value

    - Set `TRACE_MATCH_INTERRUPT` to enable interrupt match mode:
        - Configure `TRACE_MATCH_VALUE_INTERRUPT` to specify interrupt level

    - Set `TRACE_MATCH_COMP` to enable comparator match mode:
        - Configure the primary comparator:
            * Configure `TRACE_P_INPUT` to choose the input
            * Configure `TRACE_P_FUNCTION` to select the comparator function
            * Configure `TRACE_FILTER_P_COMPARATOR_MATCH_REG` to define match value

        - Configure the secondary comparator if needed:
            * Configure `TRACE_S_INPUT` to choose the input
            * Configure `TRACE_S_FUNCTION` to select the comparator function
            * Configure `TRACE_FILTER_S_COMPARATOR_MATCH_REG` to define match value

        - Choose which comparator to match via `TRACE_MATCH_MODE`
```