

```markdown
A stuff error occurs when six consecutive bits of the same value are detected (which violates the bit-stuffing encoding rules).

CRC Error
The receiver will calculate the CRC value based on the valid bits of received data frames and remote frames (before bit stuffing). A CRC Error occurs when the CRC calculated by the receiver does not match the CRC sequence in the received data frames and remote frames.

Format Error
A Format Error occurs when a format-fixed bit field of a message contains an illegal bit. For example, the r1 and r0 fields must be dominant.

ACK Error
An ACK Error occurs when a transmitter does not detect a dominant bit at the ACK Slot.
```

```markdown
## 53.2.3.2 Error States

TWAI nodes implement fault confinement by maintaining two error counters in each node, where the counter values determine the error state. The two error counters are known as the Transmit Error Counter (TEC) and Receive Error Counter (REC). TWAI has the following error states:

### Error Active
An Error Active node is able to participate in bus communication and transmit an Active Error Flag when it detects an error.

### Error Passive
An Error Passive node is able to participate in bus communication and transmit a Passive Error Flag when it detects an error. Error Passive nodes that have transmitted data or remote frames must also include the Suspend Transmission field in the subsequent Interframe Space.

### Bus Off
A Bus Off node is not permitted to influence the bus in any way (i.e., is not allowed to transmit data).
```

```markdown
## 53.2.3.3 Error State Transition

1. A node becomes Error Passive when its TEC and/or REC is greater than or equal to 128. Though the node becomes Error Passive, it still sends an Active Error Flag. Note that once the REC has reached 128, any further increases to its value are invalid until the REC returns to a value less than 128.
2. A node becomes Bus Off when its TEC is greater than or equal to 256.
3. An Error Passive node becomes Error Active when both the TEC and REC are less than or equal to 127.
4. A Bus Off node can become Error Active (with both its TEC and REC reset to 0) after it monitors 128 occurrences of 11 consecutive recessive bits on the bus.
```

```markdown
## 53.2.3.4 Error Counter Rules

The TEC and REC are incremented/decremented according to the following rules. Note that more than one rule can apply to a given message transfer.

TEC increment/decrement rules:
```