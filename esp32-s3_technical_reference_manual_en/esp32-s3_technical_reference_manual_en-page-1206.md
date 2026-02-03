**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Body Text:**

- **Endianness:** The endianness is identical to the register layout of the Receive Buffer registers. The Receive Buffer registers are mapped to the bytes of the first message in the Receive FIFO.

- When the TWAI controller receives a message, it will increment the value of `TWAI_RX_MESSAGE_COUNTER` up to a maximum of 64. If there is adequate space in the Receive FIFO, the message contents will be written into the Receive FIFO. Once a message has been read from the Receive Buffer, then `TWAI_RELEASE_BUF` bit should be set. This will decrement `TWAI_RX_MESSAGE_COUNTER` and free up to the first message in the Receive FIFO.

- A data overrun occurs when the TWAI controller receives messages but lacks adequate space for storing received messages (either due to large content or full FIFO). When a data overrun happens:
  - The free space left is filled with partial contents of the overrun message. If the FIFO is already fully occupied, all overrun messages will be stored.
  - A Data Overrun Interrupt occurs when data in the FIFO overruns for the first time.

- Each overrun incrementally increases `TWAI_RX_MESSAGE_COUNTER` up to a maximum value (64).
  
- The RX FIFO internally marks overrun messages as invalid. This can help determine if the message is valid or an overrun occurred.
  - To clear an overrun, call `TWAI_RELEASE_BUF` repeatedly until it reaches zero.

**Subsection Title:**
31.5.6 Acceptance Filter

**Body Text for Subsection:**

The Acceptance Filter allows TWAI controller to filter out received messages based on their ID (and optionally first data byte and frame type). Only accepted messages are passed onto the Receive FIFO.
- The use of acceptance filters reduces operation load by using fewer receive interrupts since only a subset is handled.

**Configuration Details for Subsection:**

The Acceptance Filter configuration registers can be accessed while TWAI controller in Reset Mode, as they share address spaces with Transmit Buffer and Receive Buffer registers. Configuration consists:
  - A 32-bit Acceptance Code Value
  - An 8-bit Acceptance Mask Value

- The acceptance code specifies which bits of the message must match for it to be accepted.
- The mask value can hide certain parts (e.g., "Don't Care").
  
**Figure Description:**
Figure 31.5-1 shows an example flowchart illustrating how messages are filtered based on their ID and data bytes.

**Footer Information:** 
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback