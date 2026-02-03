**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Table Title and Content:**
- **Table 18.4-4. The Storage and Length of Message digest from Different Algorithms**

| Hash Algorithm | Length of Message Digest (in bits) | Storage¹ |
|----------------|-------------------------------------|---------|
| SHA-1          | 160                                 | SHA_H_0_REG ~ SHA_H_4_REG       |
| SHA-224        | 224                                 | SHA_H_0_REG ~ SHA_H_6_REG       |
| SHA-256        | 256                                 | SHA_H_0_REG ~ SHA_H_7_REG       |
| SHA-384        | 384                                 | SHA_H_0_REG ~ SHA_H_11_REG      |
| SHA-512        | 512                                 | SHA_H_0_REG ~ SHA_H_15_REG      |
| SHA-512/224   | 224                                 | SHA_H_0_REG ~ SHA_H_6_REG       |
| SHA-512/256   | 256                                 | SHA_H_0_REG ~ SHA_H_7_REG       |
| SHA-512/t²     | t                                  | SHA_H_x_REG                      |

**Footnotes:**
¹ The message digest are stored in registers from most significant bits to the least significant bits, with the first word stored in register SHA_H_0_REG and the second word stored in register SHA_H_1_REG... For details, please see subsection 18.4.1.2.

² The registers used for SHA-512/t algorithm depend on the value of t. x+1 indicates the number of 32-bit registers used to store t bits of message digest, so that x = roundup(t/32).

**Example Explanation:**
For example:
- When t = 8, then x = 0, indicating that the 8-bit long message digest is stored in the most significant 8 bits of register SHA_H_0_REG;
- When t = 32, then x = 0, indicating that the 32-bit long message digest is stored in register SHA_H_0_REG;
- When t = 132, then x = 4, indicating that the 132-bit long message digest is stored in registers SHA_H_0_REG, SHA_H_1_REG, SHA_H_2_REG, SHA_H_3_REG and SHA_H_4_REG.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback