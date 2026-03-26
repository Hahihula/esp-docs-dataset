

```markdown
## 25.6 DMA-AES Working Mode

In the DMA-AES working mode, the AES accelerator supports six block cipher modes: ECB, CBC, OFB, CTR, CFB8, and CFB128. Users can choose the block cipher mode by configuring the `AES_BLOCK_MODE_REG` register according to Table 25.6-1 below.

Table 25.6-1. Block Cipher Mode

| AES_BLOCK_MODE_REG[2:0] | Block Cipher Mode                     |
|-------------------------|----------------------------------------|
| 0                       | ECB (Electronic Codebook)              |
| 1                       | CBC (Cipher Block Chaining)            |
| 2                       | OFB (Output Feedback)                  |
| 3                       | CTR (Counter)                          |
| 4                       | CFB8 (8-bit Cipher Feedback)           |
| 5                       | CFB128 (128-bit Cipher Feedback)       |
| 6                       | GCM (Galois/Counter Mode)              |
| 7                       | reserved                               |

Users can check the working status of the AES accelerator by inquiring the `AES_STATE_REG` register and comparing the return value against the Table 25.6-2 below.

Table 25.6-2. Working Status under DMA-AES Working mode

| AES_STATE_REG[1:0] | Status   | Description                                       |
|--------------------|----------|---------------------------------------------------|
| 0                  | IDLE     | The AES accelerator is idle.                      |
| 1                  | WORK     | The AES accelerator is in the middle of an operation. |
| 2                  | DONE     | The AES accelerator completed operations.         |

When working in the DMA-AES working mode, the AES accelerator supports interrupt on the completion of computation. To enable this function, write 1 to the `AES_INT_ENA_REG` register. By default, the interrupt function is disabled. Also, note that the interrupt should be cleared by software after use.

### 25.6.1 Key, Plaintext, and Ciphertext

#### Block Operation

During the block operations, the AES accelerator reads source data from DMA, and writes result data to DMA after the computation.

*   For encryption, DMA reads plaintext from memory, then passes it to AES as source data. After computation, AES passes ciphertext as result data back to DMA to write into memory.
*   For decryption, DMA reads ciphertext from memory, then passes it to AES as source data. After computation, AES passes plaintext as result data back to DMA to write into memory.

During block operations, the lengths of the source data and result data are the same. The total computation time is reduced because the DMA data operation and AES computation can happen concurrently.
```