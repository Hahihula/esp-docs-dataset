**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Titles and Content:**

1. **25.5.4 Frame Data**
   - The Frame Data fields contain the payload of transmitted or received a Data Frame, and can range from 0 to 8 bytes. The number of valid bytes should be equal to the DLC. However, if the DLC is larger than 8, the number of valid bytes would still be limited to 8. Remote Frames do not have data payloads, thus the Frame Data fields will be unused.
   - For example, when transmitting a Data Frame with 5 data bytes, the CPU should write a value of 5 to the DLC field, and then fill in data bytes 1 to 5 in the Frame Data fields. Likewise, when receiving a Data Frame with a DLC of 5, only data bytes 1 to 5 will contain valid payload data for the CPU to read.

2. **25.5.5 Receive FIFO and Data Overruns**
   - The Receive FIFO is a 64-byte internal buffer used to store received messages in First In First Out order. A single received message can occupy between 3 to 13-bytes of space in the Receive FIFO, and their byte layout is identical to the register layout of the Receive Buffer registers. The Receive Buffer registers are mapped to the bytes of the first message in the Receive FIFO.
   - When the TWAI controller receives a message, it will increment the value of `TWAI_RX_MESSAGE_COUNTER` up to a maximum of 64. If there is adequate space in the Receive FIFO, the message contents will be written into the Receive FIFO. Once a message has been read from the Receive Buffer, the `TWAI_RELEASE_BUFFER` bit should be set.
   - When the TWAI controller receives a message but lacks sufficient free space to store it (either due to its size or because of fullness), the Receive FIFO marks overrun messages as invalid and increments `TWAI_RX_MESSAGE_COUNTER` up to 64.

3. **25.5.6 Acceptance Filter**
   - The Acceptance Filter allows filtering out received messages based on their ID, optionally including data byte (and frame type). Only accepted messages are passed onto the Receive FIFO.
   - Using Acceptance Filters reduces operation load by using fewer Receive FIFO entries and interrupts for TWAI controller handling a subset of valid messages. 
   - Configuration registers can only be accessed while in Reset Mode due to shared address space with Transmit Buffer and Receive Buffer.

4. **Additional Information:**
   - The registers consist of 32-bit Acceptance Code Value, the 32-bit Acceptance Mask Value.
   - The code value specifies a bit pattern that must match for message acceptance; mask values can hide certain bits (e.g., "Don't Care" bits).

**Footer:** 
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:**
543