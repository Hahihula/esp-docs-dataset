

```markdown
Figure 5.3-2. Shift Register Circuit (first 32 output)

gf_mul_66   gf_mul_157   gf_mul_87       gf_mul_131   gf_mul_143   gf_mul_198   gf_mul_113   gf_mul_187   gf_mul_98    gf_mul_43
DFF12        DFF11         DFF11           ...            ...          ...          ...          ...          ...          ...
             AND           AND              OR             OR

Input m1, m2,...,m32

Output1 ~ 32


Figure 5.3-3. Shift Register Circuit (last 12 output)

DFF12   DFF11   DFF10   DFF9     ...      DFF3    DFF2    DFF1
        Output 33 ~ 44

• Bytes [0:31] are the data bytes itself
• Bytes [32:43] are the encoded parity bytes stored in 8-bit flip-flops DFF1, DFF2, ..., DFF12 (gf_mul_n is the result of multiplying a byte of data in GF(2⁸) by αⁿ, where n is an integer).

After that, the hardware programs into eFuse the 44-byte codeword consisting of the data bytes and the parity bytes. When the eFuse block is read, the eFuse controller automatically decodes the codeword and applies error correction if needed.

Because the RS check codes are generated on the entire 32-byte eFuse block, each block can only be written once.

Since the size of BLOCK1 is less than 32 bytes, the unused bits will be treated as 0 by hardware during the RS (44, 32) encoding. Thus, the final coding result will not be affected.

Among blocks using the RS (44, 32) coding scheme, the parameters in BLOCK1 is 24 bytes, and the RS check code is 12 bytes, so BLOCK1 occupies 24 + 12 = 36 bytes in eFuse memory.

The parameter in other blocks (Block2 ~ 10) is 32 bytes respectively, and the RS check code is 12 bytes, so they occupy (32 + 12) * 9 = 396 bytes in eFuse memory.
```

## 5.4 Functional Description
```markdown
Espressif Systems                           216                          ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback               PRELIMINARY
```