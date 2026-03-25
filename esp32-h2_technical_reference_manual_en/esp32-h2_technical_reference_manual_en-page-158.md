

```markdown
## 5.3.1.4 Data Storage

Internally, eFuse uses the hardware encoding scheme to protect data from corruption. The scheme and the encoding process are invisible to users.

All BLOCK0 parameters except for EFUSE_WR_DIS are stored with four backups, meaning each bit is stored four times. This backup scheme is not visible to users.

In BLOCK0, EFUSE_WR_DIS occupies 32 bits, and other parameters takes 152 bits each. So, the total eFuse memory space occupied by BLOCK0 is 32 + 152 * 4 = 640 bits.

In BLOCK1 ~ BLOCK10, data are coded using Reed-Solomon's RS (44, 32) coding scheme that supports up to 6 bytes of automatic error correction. The primitive polynomial of RS (44, 32) is

p(x) = x⁸ + x⁴ + x³ + x² + 1.

Figure 5.3-2. Shift Register Circuit (first 32 output)

Figure 5.3-3. Shift Register Circuit (last 12 output)

As shown in Figure 5.3-2 and 5.3-3, the shift register circuit processes the 32-byte parameters using RS (44, 32) and encodes them into 44 bytes:

* Bytes [0:31] are the data itself
* Bytes [32:43] are the encoded parity bytes stored in 8-bit flip-flops DFF1, DFF2, ..., DFF12 (gf_mul_n is the result of multiplying a byte of data in GF(2⁸) by αⁿ, where n is an integer).

After that, the hardware programs into eFuse the 44-byte codeword consisting of the data bytes and the parity
```