

```markdown
Chapter 25 Elliptic Curve Digital Signature Algorithm (ECDSA)

GoBack

25.4.2.1 Writing Data

Writing data means writing data to an ECDSA memory block and using this data as the input to the ECDSA algorithm. To be specific, writing data to an ECDSA memory block means writing D[n][31:0] to the "starting address of this ECDSA memory block + 4 × n". For a 256-bit long data example:

- write D[0] to "starting address"
- write D[1] to "starting address + 4"
- ...
- write D[7] to "starting address + 28"

Note:
When the data size of 192 bits is used, you need to append 0 after 192 bits of data and write 256 bits of data.

25.4.2.2 Reading Data

Reading data means reading data from the starting address of an ECDSA memory block and using this data as the output from the ECDSA algorithm. To be specific, reading data from an ECDSA memory block means reading D[n][31:0] from the "starting address of this ECDSA memory block + 4 × n". For a 256-bit long data example:

- read D[0] from "starting address"
- read D[1] from "starting address + 4"
- ...
- read D[7] from "starting address + 28"

Note:
When the data size of 192 bits is used, only use the low 192 bits (6 blocks) of data.

25.4.2.3 Padding the Message

The SHA accelerator can only process message blocks of 512 bits. Thus, all the messages should be padded to a multiple of 512 bits before the hash operation.

Suppose that the length of the message M is L_M bits. Then M shall be padded as introduced below:

1. First, append the bit "1" to the end of the message;
2. Second, append L_A bits of zeros, where L_A is the smallest, non-negative solution to the equation
   L_M + 1 + L_A ≡ 448 mod 512;
3. Last, append the 64-bit block of value equal to the number L_M expressed using a binary representation.

For more details, please refer to FIPS PUB 180-4 Spec > Section "Padding the Message".

25.4.2.4 Parsing the Message

The message and its padding must be parsed into N 512-bit message blocks: M^(1), M^(2), ..., M^(N).
```