**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Table Reference and Content:**
- **Table 31.3-4 – cont’d from previous page**

| Interframe Space | Description |
|------------------|-------------|
| Suspend Transmission | An Error Passive node that has just transmitted a message must include a Suspend Transmission field. This field consists of 8 recessive bits. Error Active nodes should not include this field. |
| Bus Idle | The Bus Idle field is of arbitrary length. Bus Idle ends when an SOF is transmitted. If a node has a pending transmission, the SOF should be transmitted at the first bit following Intermission. |

**Section Title:**
31.3.3 TWAI Errors

**Subsection 31.3.3.1 Error Types**

Bus Errors in TWAI are categorized into one of the following types:

- **Bit Error**: A Bit Error occurs when a node transmits a bit value (i.e., dominant or recessive) but the opposite bit is detected (e.g., a dominant bit is transmitted but a recessive is detected). However, if the transmitted bit is recessive and is located in the Arbitration Field or ACK Slot or Passive Error Flag, then detecting a dominant bit will not be considered a Bit Error.

- **Stuff Error**: A Stuff error is detected when 6 consecutive bits of the same value are detected (thus violating the bit-stuffing encoding rules).

- **CRC Error**: A receiver of a data or remote frame will calculate a CRC based on the bits it has received. A CRC error occurs when the CRC calculated by the receiver does not match the CRC sequence in the received data or remote Frame.

- **Format Error**: A Format Error is detected when a fixed-form bit field of a message contains an illegal bit. For example, the r1 and r0 fields must be dominant.

- **ACK Error**: An ACK Error occurs when a transmitter does not detect a dominant bit at the ACK Slot.

**Subsection 31.3.3.2 Error States**

TWAI nodes implement fault confinement by each maintaining two error counters, where the counter values determine the error state. The two error counters are known as the Transmit Error Counter (TEC) and Receive Error Counter (REC). TWAI has the following error states:

- **Error Active**: An Error Active node is able to participate in bus communication and transmit an Active Error Flag when it detects an error.

- **Error Passive**: An Error Passive node is able to participate in bus communication, but can only transmit a Passive Error Flag when it detects an error. Error Passive nodes that have transmitted data or remote frame must also include the Suspend Transmission field in the subsequent Interframe Space.

**Footer:**
Espressif Systems  
1192 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)