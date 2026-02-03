**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Table Header:**
Table 31.3-2. Error Frame

**Error Frame Table with Descriptions:**

| **Error Frame** | Description |
| --- | --- |
| **Error Flag** | The Error Flag has two forms, the Active Error Flag consisting of 6 dominant bits and the Passive Error Flag consisting of 6 recessive bits (unless overridden by dominant bits of other nodes). Active Error Flags are sent by error active nodes, whilst Passive Error Flags are sent by error passive nodes. |
| **Error Flag Superposition** | The Error Flag Superposition field meant to allow for other nodes on the bus to transmit their respective Active Error Flags. The superposition field can range from 0 to 6 bits, and ends when the first recessive bit is detected (i.e., the first it of the Delimiter). |
| **Error Delimeter** | The Delimiter field marks the end of the error/overload frame, and consists of 8 recessive bits. |

**Footer:**
Espressif Systems  
1190 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)