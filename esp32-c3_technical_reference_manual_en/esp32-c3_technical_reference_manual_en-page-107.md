

```markdown
Chapter 4 eFuse Controller (EFUSE)

BLOCK1 ~ BLOCK10 use RS (44,32) coding scheme that supports up to 6 bytes of automatic error correction.
The primitive polynomial of RS (44,32) is p(x) = x⁸ + x⁴ + x³ + x² + 1.

Figure 4.3-1. Shift Register Circuit (first 32 output)

gf_mul_66   gf_mul_157   gf_mul_87
↓           ↓            ↓
DFF12       DFF11        DFF10

gf_mul_131  gf_mul_143  gf_mul_198  gf_mul_113  gf_mul_187  gf_mul_121  gf_mul_98  gf_mul_43
↓           ↓            ↓          ↓          ↓          ↓          ↓         ↓
DFF1        ...         DFF2       DFF1

Input m1, m2,...,m32

Output1 ~ 32

Figure 4.3-2. Shift Register Circuit (last 12 output)

DFF12   DFF11   DFF10   DFF9    ...     DFF3    DFF2    DFF1
        Output 33 ~ 44

The shift register circuit shown in Figure 4.3-1 and 4.3-2 processes 32 data bytes using RS (44,32). This coding scheme encodes 32 bytes of data into 44 bytes:

• Bytes [0:31] are the data bytes itself
• Bytes [32:43] are the encoded parity bytes stored in 8-bit flip-flops DFF1, DFF2, ..., DFF12 (gf_mul_n, where n is an integer, is the result of multiplying a byte of data ...)

After that, the hardware burns into eFuse the 44-byte codeword consisting of the data bytes followed by the parity bytes.

When the eFuse block is read back, the eFuse controller automatically decodes the codeword and applies error correction if needed.

Because the RS check codes are generated on the entire 256-bit eFuse block, each block can only be written once.

4.3.2 Programming of Parameters

The eFuse controller can only program eFuse parameters in one block at a time. BLOCK0 ~ BLOCK10 share the same address range to store the parameters to be programmed. Configure parameter EFUSE_BLK_NUM
```