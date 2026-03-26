

```markdown
In BLOCK0, EFUSE_WR_DIS occupies 32 bits, and other parameters takes 152 bits each. So, the eFuse memory space occupied by BLOCK0 is 32 + 152 * 4 = 640 bits.

BLOCK1 ~ BLOCK10 use RS (44, 32) coding scheme that supports up to 6 bytes of automatic error correction. The primitive polynomial of RS (44, 32) is p(x) = x⁸ + x⁴ + x³ + x² + 1.

Figure 8.3-2. Shift Register Circuit (first 32 output)

Input m1, m2,...,m32

Output1 ~ 32

gf_mul_66
gf_mul_157
gf_mul_87
gf_mul_131
gf_mul_143
gf_mul_198
gf_mul_113
gf_mul_187
gf_mul_121
gf_mul_98
gf_mul_43
gf_mul_102

DFF12 DFF11 DFF2 DFF1

Figure 8.3-3. Shift Register Circuit (last 12 output)

DFF12 DFF11 DFF10 DFF9 ... DFF3 DFF2 DFF1

Output 33 ~ 44

The shift register circuit shown in Figure 8.3-2 and 8.3-3 processes 32 data bytes using RS (44, 32). This coding scheme encodes 32 bytes of data into 44 bytes:

* Bytes [0:31] are the data bytes itself
* Bytes [32:43] are the encoded parity bytes stored in 8-bit flip-flops DFF1, DFF2, ..., DFF12 (gf_mul_n is the result of multiplying a byte of data in GF(2⁸) by αⁿ, where n is an integer).

After that, the hardware programs into eFuse the 44-byte codeword consisting of the data bytes and the parity bytes. When the eFuse block is read, the eFuse controller automatically decodes the codeword and applies error correction if needed.

Because the RS check codes are generated on the entire 32-byte eFuse block, each block can only be written once.

Since the size of BLOCK1 is less than 32 bytes, the unused bits will be treated as 0 by hardware during the RS (44, 32) encoding. Thus, the final coding result will not be affected.
```