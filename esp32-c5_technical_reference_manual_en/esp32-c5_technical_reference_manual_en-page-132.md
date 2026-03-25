

```markdown
## 3.3 Features

* Compatible with Efficient Trace for RISC-V Version 2.0. See Table 3.3-1 for the implemented parameters
* Support for delta address mode and full address mode
* Support for a filter unit
* Support for notifying an instruction address via debug trigger or filter unit
* Support for the following sideband signals to control trace data flow:
    - Support for debugging trigger to start or stop encoder
    - When the hart is halted, the encoder can report the last packet and then stop
    - When the hart is reset, the encoder can report the last packet and then stop
    - Support for stalling the hart when trace FIFO is almost full
* Arbitrary address range of the trace memory size
* Configurable synchronization modes:
    - Synchronization counter counts by packet
    - Synchronization counter counts by cycle
    - Synchronization counter can be disabled
* Trace lost status to indicate packet loss
* Automatic restart after packet loss
* Memory writing in the loop or non-loop mode
* Support two interrupts:
    - Triggered when the packet size exceeds the configured memory space
    - Triggered when a packet is lost
* FIFO (128 × 8 bits) to buffer packets
* AHB burst transmission with configurable burst length

Table 3.3-1. Trace Encoder Parameters

| Parameter Name | Value | Description |
|----------------|-------|-------------|
| arch_p         | 0     | Initial version |
| bpred_size_p   | 0     | Branch prediction mode is not supported |
| cache_size_p   | 0     | Jump target cache mode is not supported |
| call_counter_size_p | 0 | Implicit return mode is not supported |
| ctype_width_p  | 0     | Width of the ctype bus |
| context_width_p| 0     | Width of context bus |
| ecause_width_p | 6     | Width of exception cause |
| ecause_choice_p| 0     | Multiple choice is not supported |
| fOs_width_p    | 0     | Format O packets are not supported |
| filter_context_p| 0   | Filtering on context is not supported |
```