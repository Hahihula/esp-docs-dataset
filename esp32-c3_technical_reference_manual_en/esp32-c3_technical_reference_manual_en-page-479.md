

```markdown
## 18.5.2 Endianness

Under the DMA-AES working mode, the transmission of source data and result data for AES Accelerator is solely controlled by DMA. Therefore, the AES Accelerator cannot control the Endianness of the source data and result data, but does have requirement on how these data should be stored in memory and on the length of the data.

For example, let us assume DMA needs to write the following data into memory at address 0x0280.
* Data represented in hexadecimal:
    - 010203040506070809A0B0C0D0E0F101112131415161718191A1B1C1D1E1F20
* Data Length:
    - Equals to 2 blocks.

Then, this data will be stored in memory as shown in Table 18.5-4 below.

Table 18.5-4. Text Endianness for DMA-AES

| Address | Byte | Address | Byte | Address | Byte | Address | Byte |
|---------|------|---------|------|---------|------|---------|------|
| 0x0280  | 0x01 | 0x0281  | 0x02 | 0x0282  | 0x03 | 0x0283  | 0x04 |
| 0x0284  | 0x05 | 0x0285  | 0x06 | 0x0286  | 0x07 | 0x0287  | 0x08 |
| 0x0288  | 0x09 | 0x0289  | 0x0A | 0x028A  | 0x0B | 0x028B  | 0x0C |
| 0x028C  | 0x0D | 0x028D  | 0x0E | 0x028E  | 0x0F | 0x028F  | 0x10 |
| 0x0290  | 0x11 | 0x0291  | 0x12 | 0x0292  | 0x13 | 0x0293  | 0x14 |
| 0x0294  | 0x15 | 0x0295  | 0x16 | 0x0296  | 0x17 | 0x0297  | 0x18 |
| 0x0298  | 0x19 | 0x0299  | 0x1A | 0x029A  | 0x1B | 0x029B  | 0x1C |
| 0x029C  | 0x1D | 0x029D  | 0x1E | 0x029E  | 0x1F | 0x029F  | 0x20 |

## 18.5.3 Standard Incrementing Function

AES accelerator provides two Standard Incrementing Functions for the CTR block operation, which are INC₃₂ and INC₁₂₈ Standard Incrementing Functions. By setting the AES_INC_SEL_REG register to 0 or 1, users can choose the INC₃₂ or INC₁₂₈ functions respectively. For details on the Standard Incrementing Function, please see Chapter B.1 The Standard Incrementing Function in NIST SP-800-38A.

## 18.5.4 Block Number

Register AES_BLOCK_NUM_REG stores the Block Number of plaintext P or ciphertext C. The length of this register equals to length(TEXT-PADDING(P))/128 or length(TEXT-PADDING(C))/128. The AES Accelerator only uses this register when working in the DMA-AES mode.

## 18.5.5 Initialization Vector

AES_IV_MEM is a 16-byte memory, which is only available for AES Accelerator working in block operations. For CBC/OFB/CFB8/CFB128 operations, the AES_IV_MEM memory stores the Initialization Vector (IV). For the CTR operation, the AES_IV_MEM memory stores the Initial Counter Block (ICB).
```