**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Heading: Overload Frames**

**Body Text:**
An overload frame has the same bit fields as an error frame containing an Active Error Flag. The key difference is in the conditions that can trigger the transmission of an overload frame. Figure 31.3-3 below shows the bit fields of an overload frame.

**Figure Caption and Description (Figure 31.3-3):**
Fields of an Overload Frame

**Table Title: Table 31.3-3. Overload Frame**

| Overload Flag | Description |
| --- | --- |
| **Overload Flag** | Consists of 6 dominant bits. Same as Active Error Flag. |
| **Overload Flag Superposition** | Allows for the superposition of Overload Flags from other nodes, similar to an Error Flag Superposition. |
| **Overload Delimiter** | Consists of 8 recessive bits. Same as an Error Delimiter. |

**Body Text:**
Overload frames will be transmitted under the following conditions:
1. A receiver requires a delay of the next data or remote frame.
2. A dominant bit is detected at the first and second bit of intermission.
3. A dominant bit is detected at the eighth (last) bit of an Error Delimiter.

**Note:**
TEC and REC will not be incremented, see Section 31.3.3 for more details).

Transmitting an overload frame due to one of the conditions must also satisfy the following rules:
- Transmitting an overload frame due to condition 1 must only be started at the first bit of intermission.
- Transmitting an overload frame due to condition 2 and 3 must start one bit after detecting the dominant bit of the condition.

A maximum of two overload frames may be generated in order to delay the next data or remote frame.

**Subsection Title: Interframe Space**

**Body Text:**
The Interframe Space acts as a separator between frames. Data frames and remote frames must be separated from preceding frames by an Interframe Space, regardless of the preceding frame’s type (data frame, remote frame, error frame, overload frame). However, error frames and overload frames do not need to be separated from preceding frames.

**Figure Caption:**
Figure 31.3-4 shows the fields within an Interframe Space:

**Table Title: Table 31.3-4. Interframe Space**

| Interframe Space | Description |
| --- | --- |
| **Intermission** | The intermission consists of 3 recessive bits.

**Footer Text:** 
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)