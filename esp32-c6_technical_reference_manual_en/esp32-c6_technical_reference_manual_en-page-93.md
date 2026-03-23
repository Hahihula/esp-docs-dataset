

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE)

GoBack



For detailed descriptions of the above parameters, please refer to the RISC-V Processor Trace Version 1.0 > Chapter Parameters and Discovery.



## 2.4 Architectural Overview

As shown in Figure 2.0-1, the trace encoder contains an encoder, a FIFO, a register configuration module, and a transmission control module.

The encoder receives HP CPU’s instruction information via the instruction trace interface, compresses it into different packets, and writes it to the internal FIFO.

The transmission control module writes the data in the FIFO to the internal SRAM through the AHB bus.

The FIFO is 128 deep and 8-bit wide. When the memory bandwidth is insufficient, the FIFO may overflow and packet loss occurs. If a packet is lost, the encoder will send a packet to tell that a packet is lost, and will stop working until the FIFO is empty.



## 2.5 Functional Description



### 2.5.1 Synchronization

In order to make the trace robust there must be regular synchronization points within the trace.

Synchronization is accomplished by sending a full valued instruction address. When the synchronization counter value reaches the value of the `TRACE_RESYNC_PROLONGED` field of the `TRACE_RESYNC_PROLONGED_REG` register, the encoder will send a synchronization packet (format 3 subformat 0, see Section 2.6.3.1).

There are two synchronization modes configured via `TRACE_RESYNC_MODE`:

*   0: Synchronization counter counts by cycle
*   1: Synchronization counter counts by packet

You can adjust the trace bandwidth by increasing the value of `TRACE_RESYNC_PROLONGED_REG` to reduce the frequency of sending synchronization packets, thereby reducing the bandwidth occupied by packets.



### 2.5.2 Anchor Tag

Since the length of data packets is variable, in order to identify boundaries between data packets when packed packets are written to memory, ESP32-C6 inserts zero bytes between data packets:

*   The maximum packet length is 13 bytes, so a sequence of at least 14 zero bytes cannot occur within a packet. Therefore, the first non-zero byte seen after a sequence of at least 14 zero bytes must be the first byte of a packet.
*   Every time when 128 packets are transmitted, the encoder writes 14 zero bytes to the memory partition boundary as anchor tags.



Espressif Systems
93
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```