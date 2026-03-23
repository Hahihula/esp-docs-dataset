

```markdown
Both IV and ICB are 128-bit strings, which can be divided into Byte0, Byte1, Byte2 … Byte15 (from left to right). AES_IV_MEM stores data following the Endianness pattern presented in Table 18.5-4, i.e. the most significant (i.e., left-most) byte Byte0 is stored at the lowest address while the least significant (i.e., right-most) byte Byte15 at the highest address.

For more details on IV and ICB, please refer to NIST SP 800-38A.
```

```markdown
## 18.5.6 Block Operation Process

1. Select one of DMA channels to connect with AES, configure the DMA chained list, and then start DMA. For details, please refer to Chapter 2 GDMA Controller (GDMA).

2. Initialize the AES accelerator-related registers:

    * Write 1 to the `AES_DMA_ENABLE_REG` register.
    * Configure the `AES_INT_ENA_REG` register to enable or disable the interrupt function.
    * Initialize registers `AES_MODE_REG` and `AES_KEY_n_REG`.
    * Select block cipher mode by configuring the `AES_BLOCK_MODE_REG` register. For details, see Table 18.5-1.
    * Initialize the `AES_BLOCK_NUM_REG` register. For details, see Section 18.5.4.
    * Initialize the `AES_INC_SEL_REG` register (only needed when AES Accelerator is working under CTR block operation).
    * Initialize the `AES_IV_MEM` memory (This is always needed except for ECB block operation).

3. Start operation by writing 1 to the `AES_TRIGGER_REG` register.

4. Wait for the completion of computation, which happens when the content of `AES_STATE_REG` becomes 2 or the AES interrupt occurs.

5. Check if DMA completes data transmission from AES to memory. At this time, DMA had already written the result data in memory, which can be accessed directly. For details on DMA, please refer to Chapter 2 GDMA Controller (GDMA).

6. Clear interrupt by writing 1 to the `AES_INT_CLR_REG` register, if any AES interrupt occurred during the computation.

7. Release the AES Accelerator by writing 0 to the `AES_DMA_EXIT_REG` register. After this, the content of the `AES_STATE_REG` register becomes 0. Note that, you can release DMA earlier, but only after Step 4 is completed.
```

```markdown
## 18.6 Memory Summary

The addresses in this section are relative to the AES accelerator base address provided in Table 3.3-3 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```

```markdown
| Name        | Description | Size (byte) | Starting Address | Ending Address | Access |
|-------------|-------------|-------------|------------------|----------------|--------|
| AES_IV_MEM  | Memory IV   | 16 bytes    | 0x0050           | 0x005F         | R/W    |
```

```markdown
Espressif Systems                         480

Submit Documentation Feedback            ESP32-C3 TRM (Version 1.3)
```