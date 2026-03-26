

```markdown
## 29.4.1.1 Padding the Message

The SHA accelerator can only process message blocks of 512 or 1024 bits, depending on the algorithm. Thus, all the messages should be padded to a multiple of 512 bits or 1024 bits before the hash operation.

Suppose that the length of the message M is m bits. Then M shall be padded as introduced below:

* SHA-1, SHA-224 and SHA-256

    1. First, append the bit "1" to the end of the message;
    2. Second, append k bits of zeros, where k is the smallest, non-negative solution to the equation m + 1 + k ≡ 448 mod 512;
    3. Last, append the 64-bit block of value equal to the number m expressed using a binary representation.

* SHA-384, SHA-512, SHA-512/224, SHA-512/256 and SHA-512/t

    1. First, append the bit "1" to the end of the message;
    2. Second, append k zero bits, where k is the smallest, non-negative solution to the equation m + 1 + k ≡ 896 mod 1024;
    3. Last, append the 128-bit block of value equal to the number m expressed using a binary representation.

For more details, please refer to FIPS PUB 180-4 Spec > Section "Padding the Message".

## 29.4.1.2 Parsing the Message

The message and its padding must be parsed into N 512-bit or 1024-bit blocks. During the task, all the message blocks should be written into the SHA_M_n_REG.

* For SHA-1, SHA-224 and SHA-256:

    The message and its padding are parsed into N 512-bit blocks, M^(1), M^(2), ..., M^(N). Since the 512 bits of the input block may be expressed as sixteen 32-bit words, the first 32 bits of message block i are denoted M₀^(i), the next 32 bits are M₁^(i), and so on up to M₁₅^(i).

    During the task, M₀^(i) should be stored in SHA_M_O_REG, M₁^(i) stored in SHA_M_1_REG, ..., and M₁₅^(i) stored in SHA_M_15_REG.

* For SHA-384, SHA-512, SHA-512/224, SHA-512/256 and SHA-512/t:

    The message and its padding are parsed into N 1024-bit blocks. Since the 1024 bits of the input block may be expressed as sixteen 64-bit words, the first 64 bits of message block i are denoted M₀^(i), the next 64 bits are M₁^(i), and so on up to M₁₅^(i).

    During the task, the most significant 32 bits and the least significant 32 bits of M₀^(i) should be stored in SHA_M_O_REG and SHA_M_1_REG, respectively, ..., the most significant 32 bits and the least significant 32 bits of M₁₅^(i) should be stored in SHA_M_30_REG and SHA_M_31_REG, respectively.

**Note:**

For more information about "message block", please refer to FIPS PUB 180-4 Spec > Section "Glossary of Terms and Acronyms".
```