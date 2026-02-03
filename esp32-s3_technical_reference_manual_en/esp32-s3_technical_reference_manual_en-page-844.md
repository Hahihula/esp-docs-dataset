**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Body Text:**
Users can start the SHA accelerator with different working modes by configuring registers `SHA_START_REG` and `SHA_DMA_START_REG`. For details, please see Table 18.3-1.

**Table Titles & Content:**

1. **Table Title:** Table 18.3-1. SHA Accelerator Working Mode
   - **Columns:** Working Mode | Configuration Method
     - Typical SHA: Set `SHA_START_REG` to 1
     - DMA-SHA: Set `SHA_DMA_START_REG` to 1

2. **Table Title:** Table 18.3-2. SHA Hash Algorithm Selection
   - **Columns:** Hash Algorithm, SHA_MODE_REG Configuration
     - SHA-1: 0
     - SHA-224: 1
     - SHA-256: 2
     - SHA-384: 3
     - SHA-512: 4
     - SHA-512/224: 5
     - SHA-512/256: 6
     - SHA-512/t: 7

**Notice Box Content:** 
ESP32-S3’s Digital Signature (DS) and HMAC Accelerator (HMAC) modules also call the SHA accelerator. Therefore, users cannot access the SHA accelerator when these modules are working.

**Subsection Title & Body Text:**
18.4 Function Description
SHA accelerator can generate the message digest via two steps: Preprocessing and Hash operation

**Subsection Subtitle:** 18.4.1 Preprocessing
- **Body Text:** Preprocessing consists of three steps: padding the message, parsing the message into message blocks and setting the initial hash value.

**Subsection Subtitle:** 18.4.1 Padding the Message
- **Body Text:** The SHA accelerator can only process message blocks of 512 or 1024 bits, depending on the algorithm. Thus, all the messages should be padded to a multiple of 512 or 1024 bits before the hash task.
  - Suppose that the length of the message M is m bits. Then M shall be padded as introduced below:
    - SHA-1, SHA-224 and SHA-256
      1. First, append the bit “1” to the end of the message;

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)