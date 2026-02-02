**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Body Text:**

- Overload Flag, or the 8th consecutive Dominant bit following a Passive Error Flag, a Transmitter will increase its TEC by 8 and a Receiver will increase its REC by 8. Each additional eight consecutive Dominant bits will also increase the TEC for (Transmitters) or REC for (Receivers) by 8 as well.
- When a Transmitter successfully transmits a message (getting ACK and no errors until the EOF is complete), the TEC is decremented by 1, unless the TEC is already at 0.

**List:**
- If the REC was between 1 and 127, the REC is decremented by 1.
- If the REC was greater than 127, the REC is set to 127.
- If the REC was 0, the REC remains 0.

- A node becomes Error Passive when its TEC and/or REC is greater than or equal to 128. The error condition that causes a node to become Error Passive will cause the node to send an Active Error Flag. Note that once the REC has reached 128, any further increases to its value are irrelevant until the REC returns to a value less than 128.
- A node becomes Bus Off when its TEC is greater than or equal to 256.

**List:**
- An Error Passive node becomes Error Active when both the TEC and REC are less than or equal to 127. 
- A Bus Off node can become the Error Active (with both its TEC and REC reset to 0) after it monitors 128 occurrences of 11 consecutive Recessive bits on the bus.

**Subsection Title:**
25.3.4 TWAI Bit Timing

**Sub-subsection Title:**
25.3.4.1 Nominal Bit

**Body Text for Sub-subsection:**

The TWAI protocol allows a TWAI bus to operate at a particular bit rate. However, all nodes within a TWAI bus must operate at the same bit rate.

- The **Nominal Bit Rate** is defined as number of bits transmitted per second from an ideal Transmitter and without any synchronization.
- The **Nominal Bit Time** is defined as 1/Nominal Bit Rate.

A single Nominal Bit Time is divided into multiple segments, and each segment is made up of multiple Time Quanta. A *Time Quantum* is a fixed unit of time, and is implemented as some form of prescaled clock signal in each node. Figure **25.3-5** illustrates the segments within a single Nominal Bit Time.

TWAI Controllers will operate in time steps of one Time Quanta where the state of the TWAI bus is analyzed at every Time Quanta. If two consecutive Time Quantas have different bus states (i.e., Recessive to Dominant or vice versa), this will be considered an edge. When the bus is analyzed at the intersection of PBS1 and PBS2, this is considered the Sample Point and the sampled bus value is considered the value of that bit.

**Table Title:**
Table 25.3-5 Segments of a Nominal Bit Time

| Segment | Description |
|---------|-------------|
| SS      | The SS (Synchronization Segment) is 1 Time Quantum long. If all nodes are perfectly synchronized, the edge of a bit will lie in the SS. |

**Footer:**
Espressif Systems  
533 ESP32 TRM (Version 5.6)

**Button Texts:**
- Submit Documentation Feedback
- GoBack