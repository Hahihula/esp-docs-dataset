**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Section Header and Content:**

- **Subsection:** 
  - **Title:** 18.4.1.2 Parsing the Message

  - **Body Text:**
    The message and its padding must be parsed into N 512-bit or 1024-bit blocks.

    For SHA-1, SHA-224 and SHA-256:
    - the message and its padding are parsed into N 512-bit blocks,
      \( M^{(2)} \), ..., \( M^{(N)} \).
      Since the bits of the input block may be expressed as sixteen 32-bit words, 
      the first 32 bits of message block i are denoted by \( M_0^{(i)} \),
      and so on up to
      \( M_{15}^{(i)} \).

    For SHA-384, SHA-512, SHA-512/224, SHA-512/256 and SHA-512/t:
    - the message and its padding are parsed into N 1024-bit blocks.
      Since the first bits of the input block may be expressed as sixteen 
      32-bit words,
      \( M_0^{(i)} \),
      i denotes by
      \( M_{64}^{(i)} \).
      The next six 64 bits are denoted to

    During task, all message blocks written into the SHA\_M\_n\_REG for following rules below:

    For SHA-1, SHA-224 and SHA-256:
    - \( M_0^{(i)} \) is stored in SHA\_M\_O\_REG,
      \( M_{1}^{(i)} \) stored in SHA\_M\_1\_REG,...,
      and
      \( M_{15}^{(i)} \) stored in SHA\_M\_15\_REG.

    For SHA-384, SHA-512, SHA-512/224 and SHA-512/256:
    - the most significant 32 bits of \( M_0^{(i)} \) are stored in
      SHA\_M\_O\_REG and SHA\_M\_1\_REG,
      respectively,..., the least 
      significant 32 bits.
    The next six 32 bits (the last three words)
    - \( M_{64}^{(i)} \) is stored in SHA\_M\_30\_REG
    and

**Note:**
For more information about “message block”, please refer to Section "2.1 Glossary of Terms and Acronyms" in FIPS PUB 180-4 Spec.

---

**Section Header:** 
18.4.1.3 Initial Hash Value

**Body Text:**
Before hash task begins for each secure hash algorithms, the initial Hash value \( H^{(0)} \) must be set based on different algorithms,
among which SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224 and
SHA-512/256 algorithms use the initial Hash values (constant C) stored in hardware.

However,
SHA-512/t requires a distinct initial hash value for each operation 
for given t.
Simply put,
SHA-512/t is generic name of \( t \)-bit hash function based on SHA-512 whose output truncated to bits
\( t \) any positive integer without leading zero such that \( t < 512, and \( t \neq 384. The initial hash value for

**Footer:**
Espressif Systems  
Submit Documentation Feedback  

**Document Information:** 
ESP32-S3 TRM (Version 1.7)