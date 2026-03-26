

```markdown
Chapter 31 ECDSA Digital Signature Peripheral (ECDSA_DS)

GoBack

31.4.2.1 Writing Data

Writing data means writing data to an ECDSA_DS memory block and using this data as the input to ECDSA_DS.
To be specific, writing data to an ECDSA_DS memory block means writing D[n][31:0] to the "starting address of this ECDSA_DS memory block + 4 × n". For a 256-bit long data:

- write D[0] to "starting address"
- write D[1] to "starting address + 4"
- ...
- write D[7] to "starting address + 28"

Note:
When storing data, write only the data block of the required length. Do not append a 0 to the most significant bit. For example, for 192-bit data, store only the 192 bits without appending 0.

31.4.2.2 Reading Data

Reading data means reading data from the starting address of an ECDSA_DS memory block and using this data as the output from ECDSA_DS. To be specific, reading data from an ECDSA_DS memory block means reading D[n][31:0] from the "starting address of this ECDSA_DS memory block + 4 × n". For a 256-bit long data:

- read D[0] from "starting address"
- read D[1] from "starting address + 4"
- ...
- read D[7] from "starting address + 28"

Note:
When reading data, only the data block of the required length needs to be read. For example, to read 192-bit data, simply read the lower 192 bits (i.e., 6 data blocks).

31.4.2.3 Padding the Message

The SHA accelerator can only process message blocks of 512 bits. Thus, all the messages should be padded to a multiple of 512 bits before the hash operation.

Suppose that the length of the message M is L_M bits. Then M shall be padded as introduced below:

1. First, append the bit "1" to the end of the message;
2. Second, append L_A bits of zeros, where L_A is the smallest, non-negative solution to the equation
   L_M + 1 + L_A ≡ 448 mod 512;
3. Last, append the 64-bit block of value equal to the number L_M expressed using a binary representation.

For more details, please refer to FIPS PUB 180-4 Spec > Section "Padding the Message".
```