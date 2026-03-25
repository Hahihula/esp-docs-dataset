

```markdown
## Register 2.9. TRACE_TRIGGER_REG (0x0020)

| Bit | Description |
|-----|-------------|
| 31-4 | reserved |
| 3-2 | TRACE_TRIGGER_ON, TRACE_TRIGGER_OFF, TRACE_MEM_LOOP, TRACE_RESTART_ENA |
| 1 | Reset |

TRACE_TRIGGER_ON Configures whether or not to enable the trace encoder.
O: Invalid. No effect
1: Enable (WT)

TRACE_TRIGGER_OFF Configures whether to stop the trace encoder.
O: Invalid. No effect
1: Stop (WT)

TRACE_MEM_LOOP Configures memory mode.
O: Non-loop mode
1: Loop mode (R/W)

TRACE_RESTART_ENA Configures whether or not to enable the automatic restart function for the encoder.
O: Disable
1: Enable (R/W)
```

```markdown
## Register 2.10. TRACE_RESYNC_PROLONGED_REG (0x0024)

| Bit | Description |
|-----|-------------|
| 31-25 | reserved |
| 24-23 | TRACE_RESYNC_MODE |
| 22-0 | TRACE_RESYNC_PROLONGED |
| 128 | Reset |

TRACE_RESYNC_PROLONGED Configures the threshold for the synchronization counter. (R/W)

TRACE_RESYNC_MODE Configures the synchronization mode.
O: Count by cycle
1: Count by packet (R/W)
```