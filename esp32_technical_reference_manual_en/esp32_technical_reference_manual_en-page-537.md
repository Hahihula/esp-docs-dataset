**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Titles and Content:**

1. **25.4.5 Acceptance Filter**
   - The text explains that the Acceptance Filter is a programmable message filtering unit which allows the TWAI controller to accept or reject received messages based on their ID field.

2. **25.4.6 Receive FIFO**
   - This section describes the Receive FIFO as an 8-byte buffer (internal to the TWAI controller) used for storing accepted messages by the Acceptance Filter.
   - Messages in this FIFO can vary between sizes of three to thirteen bytes, and it will trigger an overrun interrupt when full or lacks space.

3. **25.5 Functional Description**
   - This section introduces two working modes: Reset Mode (TWAI_RESET_MODE bit set) for configuration changes without transmitting messages.
   - Operation Mode is used by setting the TWAI_RESET_MODE bit to 0, allowing normal operation with error signaling and message reception/transmission.

4. **25.5.1 Modes**
   - The ESP32 TWAI controller supports two modes: Reset Mode (for modification of configuration registers) which disconnects from the bus.
   - Operation Mode connects the TWAI controller to the TWAI bus, ensuring consistent operation with error signaling and message handling.

5. **25.5.1.1 Reset Mode**
   - Entering this mode is necessary for modifying various configuration registers without transmitting messages or receiving any new ones during reset operations (immediate termination of ongoing transmission).

6. **25.5.1.2 Operation Mode**
   - This section details that entering operation mode connects the TWAI controller to the bus, protecting its settings and allowing normal message handling.
   - The operating sub-mode is determined by how configuration was set up.

7. **Sub Modes:**
   - Normal Mode allows transmission/reception of messages with error signaling (Error and Overload Frames).
   - Self Test Mode operates similarly but considers Data or RTR Frame successful even if not acknowledged, useful for self-testing the TWAI controller without acknowledgment confirmation from other devices.
   
**Footer Information:**  
Espressif Systems  
Page number: 537  
Document version: ESP32 TRM (Version 5.6)  

**Navigation Links and Feedback Options:**  
- GoBack
- Submit Documentation Feedback