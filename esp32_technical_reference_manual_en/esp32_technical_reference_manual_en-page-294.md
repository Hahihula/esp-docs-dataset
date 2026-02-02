**Chapter Title:**
Chapter 16 SHA Accelerator (SHA)

**Body Text:**

SHA_TEXT_4_REG. SHA-256 produces a 256-bit message digest and stores it in SHA_TEXT_O_REG ~

SHA_TEXT_7_REG. SHA-384 produces a 384-bit message digest and stores it in SHA_TEXT_O_REG ~

SHA_TEXT_11_REG. SHA-512 produces a 512-bit message digest and stores it in SHA_TEXT_O_REG ~

SHA_TEXT_15_REG.

As described in "2.2.1 Parameters" in FIPS PUB 180-4, “H^(N)” is the final hash value, and is used to determine the message digest”, while H^(_0) is the leftmost word of hash value i”, so the leftmost word H^(_0(N)) in the message digest is stored in SHA_TEXT_O_REG. In the same fashion, the second leftmost word H^(_1(N)) in the message digest is stored in SHA_TEXT_1_REG, etc.

**Subsection Title:**
16.3.3 Hash Operation

**Body Text:**

There is a set of control registers for SHA-1, SHA-256, SHA-384 and SHA-512, respectively; different hashing algorithms use different control registers.
SHA-1 uses SHA_SHA1_START_REG, SHA_SHA1_CONTINUE_REG, SHA_SHA1_LOAD_REG and SHA_SHA1_BUSY_REG.

SHA-256 uses SHA_256_START_REG, SHA_SHA256_CONTINUE_REG,
SHA_SHA256_LOAD_REG and SHA_SHA256 BUSY_REG. SHA-384 uses SHA_SHA384_START_REG,
SHA_SHA384_CONTINUE_REG, SHA_SHA384_LOAD_REG and SHA_SHA384 BUSY_REG.
SHA-512 uses SHA_512_START_REG, SHA_SHA512_CONTINUE_REG, SHA_SHA512_LOAD_REG and SHA_SHA512 BUSY_REG. The following steps describe the operation in a detailed manner.

**List:**
1. Feed the accelerator with the first message block:
   (a) Use the first message block to initialize SHA_TEXT_n_REG.
   (b) Write 1 to SHA_X_START_REG.
   (c) Wait for SHA_X_BUSY_REG to read 0, indicating that the operation is completed.

2. Similarly, feed the accelerator with subsequent message blocks:
   (a) Initialize SHA_TEXT_n_REG using the subsequent message block.
   (b) Write 1 to SHA_X_CONTINUE_REG.
   (c) Wait for SHA_X BUSY_REG to read 0, indicating that the operation is completed.

3. Get message digest:
   (a) Write 1 to SHA_X_LOAD_REG.
   (b) Wait for SHA_X_BUSY_REG to read 0, indicating that operation is completed.
   (c) Read message digest from SHA_TEXT_n_REG.

**Subsection Title:**
16.3.4 Speed

**Body Text:**

The SHA Accelerator requires 60 to 100 clock cycles to process a message block and 8 to 20 clock cycles to calculate the final digest.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback
ESP32 TRM (Version 5.6)