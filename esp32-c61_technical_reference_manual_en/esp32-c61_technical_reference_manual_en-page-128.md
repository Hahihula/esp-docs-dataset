

```markdown
## Chapter 2 RISC-V Trace Encoder (TRACE)

The synchronization counter is configured via `TRACE_RESYNC_MODE`:

*   0: Disable the synchronization counter
*   1: Invalid. No effect
*   2: Synchronization counter counts by packet
*   3: Synchronization counter counts by cycle

You can adjust the trace bandwidth by increasing the value of `TRACE_RESYNC_PROLONGED` to reduce the frequency of sending synchronization packets, thereby reducing the bandwidth occupied by packets.

### 2.5.2 Address Mode

ESP32-C61 supports two address modes: delta address mode and full address mode.

*   **Delta address mode (default):** In delta address mode, addresses are encoded as the difference between the actual addresses of the current instruction and the actual address of the instruction reported in the previous packet that contained an address. This differential encoding requires fewer bits than the full address, and thus results in more efficient trace compression.
*   **Full address mode:** In full address mode, all addresses in the trace are encoded as absolute addresses instead of in differential form. This kind of encoding is always less efficient, but it can be a useful debugging aid for software decoder developers. This mode is enabled by setting `TRACE_FULL_ADDRESS`.

### 2.5.3 Optional Sideband Signals

The Efficient Trace for RISC-V Version 2.0 > Chapter Optional Sideband Signals has provided some optional sideband signals for encoder control. ESP32-C61 has implemented the following functions:

Table 2.5-1. Optional sideband signals

| Signal       | Function                                                                                                                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| trigger[2:0] | • A pulse on bit 0 will cause the encoder to start tracing, and continue until further notice, subject to other filtering criteria also being met.<br>• A pulse on bit 1 will cause the encoder to stop tracing until further notice.<br>• A pulse on bit 2 will cause the encoder to report a specific address. This function is enabled by setting `TRACE_DM_TRIGGER_ENA`. The trigger signal is asserted upon a trigger match. For example, if the `action` field of `mcontrol` is 2, while the trigger matched it will assert trigger bit0; if the `action` is 3, while the trigger matched it will assert trigger bit1. For details, please refer to Table 2.8-1. |
| halted       | Hart is halted. Upon assertion, the encoder will output a packet to report the address of the last instruction retired before halting, followed by a support packet to indicate that tracing has stopped. Upon deassertion, the encoder will start tracing again, commencing with a synchronization packet. This function is enabled by setting `TRACE_HALT_ENA`. |
```