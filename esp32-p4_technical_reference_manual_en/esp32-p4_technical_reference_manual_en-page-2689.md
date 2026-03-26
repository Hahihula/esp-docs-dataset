

```markdown
1. When a transmitter sends an Error Flag, the TEC is increased by 8. However, the following scenarios are exempt from this rule:

* A transmitter is Error Passive and no dominant bit is detected when an Acknowledgment Error is detected and the Passive Error Flag is sent. In this case, the TEC should not be increased.
* A transmitter transmits an Error Flag due to a Stuff Error during Arbitration. If the stuffed bit should have been recessive but was monitored as dominant, then the TEC should not be increased.

2. If a transmitter detects a Bit Error while sending an Active Error Flag or Overload Flag, the TEC is increased by 8.

3. A node can tolerate up to 7 consecutive dominant bits after sending an Active/Passive Error Flag, or Overload Flag. After detecting the 14th consecutive dominant bit when sending an Active Error Flag or Overload Flag, or the 8th consecutive dominant bit following a Passive Error Flag, a transmitter will increase its TEC by 8 and a receiver will increase its REC by 8. Every additional 8 consecutive dominant bits will also increase the TEC for transmitters or REC for receivers by 8 as well.

4. When a transmitter has transmitted a message, which means getting ACK and no errors until the EOF is completed, the TEC is decremented by 1, unless the TEC is already at 0.

REC increment/decrement rules:

1. When a receiver detects a dominant bit as the first bit after sending an Error Flag, the REC is increased by 8.
2. When a receiver detects an error, the REC is increased by 1, except when the detected error was a Bit Error during the transmission of an Active Error Flag or an Overload Flag.
3. If a receiver detects a Bit Error while sending an Active Error Flag or Overload Flag, the REC is increased by 8.
4. When a receiver successfully receives a message, which means getting no errors before ACK Slot and successfully sending ACK, the REC is decremented accordingly.

* If the REC is between 1 and 127, it will be decremented by 1.
* If the REC is greater than 127, it will be set to 127.
* If the REC is 0, it will remain 0.
```

## 53.2.4 TWAI Bit Timing

### 53.2.4.1 Nominal Bit

The TWAI protocol allows a TWAI bus to operate at a particular bit rate. However, all nodes within a TWAI bus must operate at the same bit rate.

* The **Nominal Bit Rate** is defined as the number of bits transmitted per second.
* The **Nominal Bit Time** is defined as 1/Nominal Bit Rate.

A single Nominal Bit Time is divided into multiple segments, and each segment is made up of multiple Time Quanta. A **Time Quantum** is a minimum unit of time, and is implemented as some form of prescaled clock signal in each node. Figure 53.2-5 illustrates the segments within a single Nominal Bit Time.
```