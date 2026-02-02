**Chapter Title:**
Chapter 17

**Subtitle:**
External Memory Encryption and Decryption (FLASH)

**Section Heading:**
17.1 Overview

**Body Text:**
Many variants of the ESP32 must store programs and data in external flash memory. The external flash memory chip is likely to contain proprietary firmware and sensitive user data, such as credentials for gaining access to a private network. The Flash Encryption block can encrypt code and write encrypted code to off-chip flash memory for enhanced hardware security. When the CPU reads off-chip flash through the cache, the Flash Decryption block can automatically decrypt instructions and data read from the off-chip flash, thus providing hardware-based security for application code.

**Section Heading:**
17.2 Features

**List of Features:**
- Various key generation methods
- Software-based encryption
- High-speed, hardware decryption
- Register configuration, system parameters and boot mode jointly determine the flash encryption/decryption function.

**Footer Information:**
Espressif Systems  
303 ESP32 TRM (Version 5.6)  

**Link Texts:**
GoBack

Submit Documentation Feedback