

```markdown
25.6.3 Standard Incrementing Function

AES accelerator provides two Standard Incrementing Functions for the CTR block operation, which are INC₃₂ and INC₁₂₈ Standard Incrementing Functions. By setting the AES_INC_SEL_REG register to 0 or 1, users can choose the INC₃₂ or INC₁₂₈ functions respectively. For details on the Standard Incrementing Function, please see Chapter B.1 The Standard Incrementing Function in NIST SP 800-38A.

25.6.4 Block Number

Register AES_BLOCK_NUM_REG stores the Block Number of plaintext P or ciphertext C. The length of this register equals to length(TEXT-PADDING(P))/128 or length(TEXT-PADDING(C))/128. The AES accelerator only uses this register when working in the DMA-AES mode.

25.6.5 Initialization Vector

AES_IV_MEM is a 16-byte memory, which is only available for AES accelerator working in block operations. For CBC/OFB/CFB8/CFB128 operations, the AES_IV_MEM memory stores the Initialization Vector (IV). For the CTR operation, the AES_IV_MEM memory stores the Initial Counter Block (ICB).

Both IV and ICB are 128-bit strings, which can be divided into Byte0, Byte1, Byte2 … Byte15 (from left to right). AES_IV_MEM stores data following the Endianness pattern presented in Table 25.6-4, i.e., the most significant (i.e., left-most) byte Byte0 is stored at the lowest address while the least significant (i.e., right-most) byte Byte15 at the highest address.

For more details on IV and ICB, please refer to NIST SP 800-38A.

25.6.6 Block Operation Process

1. Select one of DMA channels to connect with AES, configure the DMA linked list, and then start DMA. For details, please refer to Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI).

2. Initialize the AES accelerator-related registers:

    * Write 1 to the AES_DMA_ENABLE_REG register.
    * Configure the AES_INT_ENA_REG register to enable or disable the interrupt function.
    * Initialize registers AES_MODE_REG and AES_KEY_n_REG.
    * Select block cipher mode by configuring the AES_BLOCK_MODE_REG register. For details, see Table 25.6-1.
    * Initialize the AES_BLOCK_NUM_REG register. For details, see Section 25.6.4.
    * Initialize the AES_INC_SEL_REG register (only needed when AES accelerator is working under CTR block operation).
    * Initialize the AES_IV_MEM memory (This is always needed except for ECB block operation).

3. Start operation by writing 1 to the AES_TRIGGER_REG register.

4. Wait for the completion of computation, which happens when the content of AES_STATE_REG becomes 2 or the AES interrupt occurs.
```