

```markdown
endianess is identical to the register layout of the Receive Buffer registers. The Receive Buffer registers are mapped to the bytes of the first message in the Receive FIFO.

When the TWAI controller receives the first message, the value of `TWAI_RX_MESSAGE_COUNTER` increases to 1, and the RXI interrupt is activated, automatically updating the first message into the buffer. Subsequently, with each new message received by the TWAI controller, the value of `TWAI_RX_MESSAGE_COUNTER` increments by 1, reaching a maximum of 64. When this limit is reached and there is sufficient space remaining in the Receive FIFO, the message will be written into the FIFO.

Once the software reads a message from the Receive Buffer, it can free up the space occupied by the message in the Receive FIFO by setting `TWAI_RELEASE_BUFFER` to 1. This will also decrement `TWAI_RX_MESSAGE_COUNTER` by 1. The Receive Buffer will then map to the next message in the Receive FIFO. The software should repeat the above operations until `TWAI_RX_MESSAGE_COUNTER` reaches 0. At this point, the RXI interrupt stops being triggered, the data in the receive buffer becomes invalid, and `TWAI_STATUS_RECEIVE_BUFFER` is set to 0.

A data overrun occurs when the TWAI controller receives a message, but the Receive FIFO lacks adequate free space to store the received message in its entirety (either due to the message contents being larger than the free space in the Receive FIFO, or the Receive FIFO being completely full).

When a data overrun occurs:

* The free space left in the Receive FIFO is filled with the partial contents of the overrun message. If the Receive FIFO is already full, then none of the overrun message’s contents will be stored.
* When data in the Receive FIFO overruns for the first time, a Data Overrun Interrupt will be triggered.
* Each overrun message will still increment the `TWAI_RX_MESSAGE_COUNTER` up to a maximum of 64.
* The Receive FIFO will internally mark overrun messages as invalid. The `TWAI_STATUS_MISS` bit can be used to determine whether the message currently mapped to by the Receive Buffer is valid or overrun.

To clear an overrun Receive FIFO, the `TWAI_RELEASE_BUFFER` must be called repeatedly until `TWAI_RX_MESSAGE_COUNTER` is 0. This requires users to read all valid messages in the Receive FIFO and clear all overrun messages.
```

## 53.4.5 Acceptance Filter

The Acceptance Filter allows the TWAI controller to filter out received messages based on their ID (and optionally their first data byte and frame type). Only accepted messages are passed on to the Receive FIFO. The use of Acceptance Filters allows a more lightweight operation of the TWAI controller (e.g., less use of Receive FIFO, fewer Receive Interrupts) since the TWAI Controller only needs to handle a subset of messages.

The Acceptance Filter configuration registers can only be accessed whilst the TWAI controller is in Reset mode, since they share the same address spaces with the Transmit Buffer and Receive Buffer registers.

The configuration registers consist of a 32-bit Acceptance Code Value and a 32-bit Acceptance Mask Value. The Acceptance Code value specifies a bit pattern which each filtered bit of the message must match in order for the message to be accepted. The Acceptance Mask Value is able to mask out certain bits of the Code value (i.e., set as “Don’t Care” bits). Each filtered bit of the message must either match the acceptance code or be masked in order for the message to be accepted, as demonstrated in Figure 53.4-1.
```