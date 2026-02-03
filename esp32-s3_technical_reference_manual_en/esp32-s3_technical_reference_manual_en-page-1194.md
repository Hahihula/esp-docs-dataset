**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Header:**
Bus Off

**Body Text:**
A Bus Off node is not permitted to influence the bus in any way (i.e., is not allowed to transmit anything).

**Subsection Title:**
31.3.3 Error Counters

**Body Text:**
The TEC and REC are incremented/decremented according to the following rules. Note that more than one rule can apply for a given message transfer.

- When a receiver detects an error, the REC is increased by 1, except when the detected error was a Bit Error during the transmission of an Active Error Flag or an Overload Flag.
- When a receiver detects a dominant bit as the first bit after sending an Error Flag, the REC is increased by 8.
- When a transmitter sends an Error Flag, the TEC is increased by 8. However, the following scenarios are exempt from this rule:
  - If a transmitter is Error Passive that detects an Acknowledgment Error due to not detecting a dominant bit in the ACK Slot, it should send a Passive Error Flag. If no dominant bit is detected in that Passive Error Flag, the TEC should not be increased.
- A transmitter transmits an Error Flag due to a Stuff Error during Arbitration. If the offending bit should have been recessive but was monitored as dominant, then the TEC should not be increased.

**Additional Rules:**
1. If a transmitter detects a Bit Error whilst sending an Active Error Flag or Overload Flag, the TEC is increased by 8.
2. A node can tolerate up to 7 consecutive dominant bits after sending an Active/Passive Error Flag, or Overload Flag. After detecting the 14th consecutive dominant bit (when sending an Active Error Flag or Overload Flag), or the 8th consecutive dominant bit following a Passive Error Flag, a transmitter will increase its TEC by 8 and every receiver will increase its REC by 8.
3. Every additional eight consecutive dominant bits will also increase the TEC for transmitters) or REC (for receivers) by 8 as well.

**Additional Rules:**
4. When a transmitter successfully transmits a message (getting ACK and no errors until the EOF is complete), the TEC is decremented by 1, unless the TEC is already at 0.
5. When a receiver successfully receives a message (no errors before ACK Slot, and successful sending of ACK), the REC is decremented.

**Additional Rules:**
- If the REC was between 1 and 127, the REC is decremented by 1.
- If the REC was greater than 127, the REC is set to 127.
- If the REC was O, the REC remains O. 

6. A node becomes Error Passive when its TEC and/or REC are greater than or equal to 128. The error condition that causes a node to become Error Passive will cause the node to send an Active Error Flag.

**Additional Rules:**
- Note that once the REC has reached to 128, any further increases to its value are invalid until the REC returns to a value less than or equal to 128.
7. A node becomes Bus Off when its TEC is greater than or equal to 256.

**Additional Rules:**
- An Error Passive node becomes Error Active when both the TEC and REC are less than or equal to 127.

**Footer Information:**
Espressif Systems
Page Number: 1194
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- GoBack
- Submit Documentation Feedback