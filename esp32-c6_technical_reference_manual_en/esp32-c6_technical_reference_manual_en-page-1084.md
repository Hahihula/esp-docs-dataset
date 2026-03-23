

```markdown
first message in the Receive FIFO. The Receive Buffer will then map to the next message in the Receive FIFO.

A data overrun occurs when the TWAI controller receives a message, but the Receive FIFO lacks adequate free space to store the received message in its entirety (either due to the message contents being larger than the free space in the Receive FIFO, or the Receive FIFO being completely full).

When a data overrun occurs:

* The free space left in the Receive FIFO is filled with the partial contents of the overrun message. If the Receive FIFO is already full, then none of the overrun message's contents will be stored.
* When data in the Receive FIFO overruns for the first time, a Data Overrun Interrupt will be triggered.
* Each overrun message will still increment the TWAI_RX_MESSAGE_COUNTER up to a maximum of 64.
* The Receive FIFO will internally mark overrun messages as invalid. The TWAI_MISS_ST bit can be used to determine whether the message currently mapped to by the Receive Buffer is valid or overrun.

To clear an overrun Receive FIFO, the TWAI_RELEASE_BUF must be called repeatedly until TWAI_RX_MESSAGE_COUNTER is 0. This requires users to read all valid messages in the Receive FIFO and clear all overrun messages.

## 33.4.6 Acceptance Filter

The Acceptance Filter allows the TWAI controller to filter out received messages based on their ID (and optionally their first data byte and frame type). Only accepted messages are passed on to the Receive FIFO. The use of Acceptance Filters allows a more lightweight operation of the TWAI controller (e.g., less use of Receive FIFO, fewer Receive Interrupts) since the TWAI Controller only need to handle a subset of messages.

The Acceptance Filter configuration registers can only be accessed whilst the TWAI controller is in Reset Mode, since they share the same address spaces with the Transmit Buffer and Receive Buffer registers.

The configuration registers consist of a 32-bit Acceptance Code Value and a 32-bit Acceptance Mask Value. The Acceptance Code value specifies a bit pattern which each filtered bit of the message must match in order for the message to be accepted. The Acceptance Mask Value is able to mask out certain bits of the Code value (i.e., set as “Don’t Care” bits). Each filtered bit of the message must either match the acceptance code or be masked in order for the message to be accepted, as demonstrated in Figure 33.4-1.

![Figure 33.4-1. Acceptance Filter](image_path) (Note: Actual image not included here; description follows)

```
Figure 33.4-1 shows a logic diagram of the acceptance filter operation:

- A "message bit" is compared with an "acceptance code bit".
- The result passes through an XNOR gate.
- An "acceptance mask bit" controls whether this comparison should be inverted (via XOR).
- These results are combined via OR gates and then ANDed together to produce a final output: `1 = accepted`, `0 = not accepted`.

```markdown
Espressif Systems    1084
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```