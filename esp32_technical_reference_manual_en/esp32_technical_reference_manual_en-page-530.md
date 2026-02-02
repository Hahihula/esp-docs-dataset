**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Table Titles and Content:**

1. **Table 25.3-2. Error Frame**
   - **Error Flag Description:** The Error Flag has two forms, the Active Error Flag consisting of 6 Dominant bits and the Passive Error Flag consisting of 6 Recessive bits (unless overridden by Dominant bits of other nodes). Active Error Flags are sent by Error Active nodes; whilst Passive Error Flags are sent by Error Passive nodes.
   - **Error Flag Superposition Description:** The Error Flag Superposition field meant to allow for other nodes on the bus to transmit their respective Active Error Flags. The superposition field can range from 0 to 6 bits, and ends when the first Recessive bit is detected (i.e., the first it of the Delimiter).
   - **Error Delimiter Description:** The Delimiter field marks the end of the Error/Overload Frame; consists of 8 Recessive bits.

2. **Table 25.3-3. Overload Frames**
   - An Overload Frame has the same bit fields as an Error Frame containing an Active Error Flag.
   - Key difference is in conditions that can trigger transmission:
     - Figure shows: The Bit Fields of an Overload Frame (Overload Frame, Overload Flag 6 bits, Overload Flag Superposition 0 to 6 bits, and Overload Delimiter 8 bits).

3. **Table 25.3-4. Overload Frame Description**
   - Consists:
     - Overload Flag: Same as an Active Error Flag.
     - Overload Flag Superposition allows for the superposition of Overload Flags from other nodes similar to an Error Flag Superposition, consisting also of Recessive bits (8).
   
**Additional Information on Overload Frames Transmission Conditions and Rules:** 
- **Conditions under which Overload Frames will be transmitted:**
  1. The internal conditions of a Receiver requires delay in the next Data or Remote Frame.
  2. Detection of Dominant bit at first second intermission bits
  3. If dominant is detected last (8th) bit Error Delimiter, TEC and REC not incremented.

- **Rules for transmitting an overload frame:**
  - Transmitting due to condition must start from the Intermission's beginning.
  - Transmitting after detecting Dominant of conditions starts one bit later than detection in error flag. 

**Footer Information:** 
Espressif Systems
530 ESP32 TRM (Version 5.6)
Submit Documentation Feedback