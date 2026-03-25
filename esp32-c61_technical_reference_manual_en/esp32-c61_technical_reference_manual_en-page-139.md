

```markdown
- There are 2 ways to enable the trace encoder:
    - Setting the `TRACE_TRIGGER_ON` bit of `TRACE_TRIGGER_REG`
    - Through the Debug module by configuring Trace-on trigger action to start the encoder. When the trigger is matched and the `action` is 2, it will start the encoder. For trigger configurations, please refer to the RISC-V Debug Specification.

Once the encoder is enabled, it will keep tracing the HP CPU’s instruction trace interface and writing packets to the trace memory.

## 2.8.4 Disable Encoder

There are two ways to stop producing trace packets:

1. Set `TRACE_TRIGGER_OFF` of `TRACE_TRIGGER_REG` to end the encoder
2. Through the Debug module by configuring Trace-off trigger action to stop the encoder. When the trigger is matched and the `action` is 3, it will disable the encoder. For trigger configurations, please refer to the RISC-V Debug Specification.

Due to the internal FIFO, the packets are not written to the memory immediately after the end of the trace. It is recommended to query the `TRACE_FIFO_STATUS_REG` to confirm that the data is all written to memory.

Table 2.8-2. Trace Status

| Field                        | Description                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| `TRACE_FIFO_EMPTY`           | If 1 indicates that the FIFO is empty, all data have been written to memory |
| `TRACE_WORK_STATUS`          | Encoder’s work status:<br>• 0: idle state, the encoder is not started<br>• 1: the encoder is normally working that output packets<br>• 2: the encoder is not outputting packets, the CPU is halted or in reset<br>• 3: the encoder is not outputting packets, it occurs while a packet is lost, and is waiting for FIFO empty to restart |

## 2.8.5 Notify

Users may want to report a special address, even if it is not the target of an uninferable discontinuity. There are two ways to notify and report a special address:

1. The debug trigger unit matched, and the `action` is 4
2. The filter comparator matched

When a notification is requested, the encoder will report a format 2 or format 1 with an address packet, determined by the `branch_map`. If `branch_map` is 0, report format 2, otherwise report format 1. The notify field shows whether the packet is reporting a notification address. If it is the target of an uninferable discontinuity, even if it is a notification, the notify field will not be asserted, otherwise the decoder cannot reconstruct the instruction stream correctly.
```