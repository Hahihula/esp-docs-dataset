**Chapter Title:**
Chapter 16 SHA Accelerator (SHA)

**GoBack Link:** [GoBack](#)

---

### Section Heading:
16.1 Introduction

**Body Text:**
The SHA Accelerator is included to speed up SHA hashing operations significantly, compared to SHA hashing algorithms implemented solely in software. The SHA Accelerator supports four algorithms of FIPS PUB 180-4, specifically SHA-1, SHA-256, SHA-384 and SHA-512.

---

### Section Heading:
16.2 Features

**Body Text:**
Hardware support for popular secure hashing algorithms:

- SHA-1
- SHA-256
- SHA-384
- SHA-512

---

### Section Heading:
16.3 Functional Description

#### Subsection 16.3.1 Padding and Parsing the Message

**Body Text:**
The SHA Accelerator can only accept one message block at a time. Software divides the message into blocks according to “5.2 Parsing the Message” in FIPS PUB 180-4 and writes one block to the SHA_TEXT_n_REG registers each time. For SHA-1 and SHA-256, software writes a 512-bit message block to SHA_TEXT_15_REG each time. For SHA-384 and SHA-512, software writes a 1024-bit message block to SHA_TEXT_0_REG ~ SHA_TEXT_31_REG each time.

The SHA Accelerator is unable to perform the padding operation of “5.1 Padding the Message” in FIPS PUB 180-4; Note that the user software is expected to pad the message before feeding it into the accelerator.

As described in "2.2.1: Parameters" in FIPS PUB 180-4, \( M_0^{(i)} \) is the leftmost word of message block i". \( M_0^{(i)} \) is stored in SHA_TEXT_0_REG. In the same fashion, the SHA_TEXT_1_REG register stores the second left-most word of a message block \( M_1^{(N)} \), etc.

#### Subsection 16.3.2 Message Digest

**Body Text:**
When the hashing operation is finished, the message digest will be refreshed by SHA Accelerator and will be stored in SHA_TEXT_n_REG. SHA-1 produces a 160-bit message digest and stores it in SHA_TEXT_0_REG.

---

**Footer Information:** 
Espressif Systems  
293  
ESP32 TRM (Version 5.6)  

**Link:**
Submit Documentation Feedback