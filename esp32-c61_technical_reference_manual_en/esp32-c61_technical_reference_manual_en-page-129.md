

```markdown
| Signal | Function |
|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| reset | Hart is in reset. Behavior is as described above for halted. |
| stall | Stall request to hart. Some applications may require lossless trace, which can be achieved by using this signal to stall the hart if the trace encoder is unable to output a trace packet (internal FIFO almost full). This function is enabled by setting `TRACE_STALL_ENA`. |
```

### 2.5.4 Filtering

Filtering provides a mechanism to control the criteria for the encoder to produce a trace. For example, it may be desirable to trace:

* When the instruction address is within a particular range
* Starting from one instruction address and continue until a second instruction address
* For one or more specified privilege levels
* Exception and/or interrupt handlers for specified exception causes

The filtering unit has a filter and a comparator unit.

Each comparator unit is actually a pair of comparators (Primary and Secondary, or P, S) allowing a bounded range to be matched with a signal unit if required, and offers:

* Input selected from instruction address (iaddress) and trap value (tval)
* A range of arithmetic options (<, >, =, !=, etc.) independently selectable for each comparator
* Secondary match value may be used as a mask for the primary comparator
* The two comparators can be combined in several ways: `P`, `P && S`, `!(P && S)`, latch (set on P clear on S)
* Each comparator can also be used to explicitly report a particular instruction address

Each filter can specify filtering against instruction from the hart, and offers:

* 1 run-time selectable comparator units to match
* Selection for specific privilege level (priv) and exception cause (ecause) as inputs
* Select matching for interrupt

### 2.5.5 Anchor Tag

Since the length of data packets is variable, in order to identify boundaries between data packets when packed packets are written to memory, the ESP32-C61 encoder inserts zero bytes between data packets:

* The maximum packet length is 13 bytes, so a sequence of at least 14 zero bytes cannot occur within a normal packet. Therefore, the first non-zero byte seen after a sequence of at least 14 zero bytes must be the first byte of a packet.
* Every time when 128 packets are transmitted, the encoder writes 14 zero bytes to the memory partition boundary as anchor tags.
```