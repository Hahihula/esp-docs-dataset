

```markdown
- non-FIFO mode: each piece in different type of information used to establish the DCn Huffman table must be written to a specific address.
    - the number of codeword with a codeword length of 1 to 16 bits: JPEG codec base address + 0x500 + n * 0x80 + (codeword length - 1) * 0x4, in which codeword length = 1, 2, ..., 16.
    - the symbols corresponding to the decoded codeword: JPEG codec base address + 0x600 + n * 0x40 + symbol number * 0x4, in which symbol number = 0, 1, ..., 15.
    - the minimum codeword with a codeword length of 1 to 16 bits: JPEG codec base address + 0xF00 + n * 0x80 + (codeword length - 1) * 0x4, in which codeword length = 1, 2, ..., 16.

In this mode, since each piece of different type of information is written to a specific address, configuring each piece of information in sequence is not required.

- FIFO mode: all pieces of the same type of information used to establish the DCn Huffman table must be written to the same address, respectively.
    - the number of codeword with a codeword length of 1 to 16 bits: JPEG_DHT_TOTLEN_DCn_REG.
    - all symbols corresponding to the decoded codeword (DC table has up to 16 symbols): JPEG_DHT_VAL_DCn_REG.
    - the minimum codeword with a codeword length of 1 to 16 bits: JPEG_DHT_CODEMIN_DCn_REG.

In this mode, since all pieces of the same type of information are written to the same address, configuring each piece of same type of information one by one in sequence is required. Afterwards, the hardware will automatically store such information in sequence.

The configuration of ACn (n = 0, 1) tables is very similar to that of the DCn (n = 0, 1) tables. Here below is the configuration of ACn (n = 0, 1) tables:

- non-FIFO mode: each piece in different type of information used to establish the ACn Huffman table must be written to a specific address.
    - the number of codeword with a codeword length of 1 to 16 bits: JPEG codec base address + 0x540 + n * 0x80 + (codeword length - 1) * 0x4, in which codeword length = 1, 2, ..., 16.
    - the symbols corresponding to the decoded codeword: JPEG codec base address + 0x680 + n * 0x400 + symbol number * 0x4, in which symbol number = 0, 1, ..., 256.
    - the minimum codeword with a codeword length of 1 to 16 bits: JPEG codec base address + 0xF40 + n * 0x80 + (codeword length - 1) * 0x4, in which codeword length = 1, 2, ..., 16.

In this mode, since each piece of different type of information is written to a specific address, configuring each piece of information in sequence is not required.

- FIFO mode: all pieces of the same type of information used to establish the ACn Huffman table must be written to the same address, respectively.
    - the number of codeword with a codeword length of 1 to 16 bits: JPEG_DHT_TOTLEN_ACn_REG.
    - all symbols corresponding to the decoded codeword (AC table has up to 256 symbols): JPEG_DHT_VAL_ACn_REG.
    - the minimum codeword with a codeword length of 1 to 16 bits: JPEG_DHT_CODEMIN_ACn_REG.
```