

```markdown
## Table 22.6-1. Block Cipher Mode

| AES_BLOCK_MODE_REG[2:0] | Block Cipher Mode                     |
|-------------------------|---------------------------------------|
| 0                       | ECB (Electronic Codebook)             |
| 1                       | CBC (Cipher Block Chaining)           |
| 2                       | OFB (Output Feedback)                 |
| 3                       | CTR (Counter)                         |
| 4                       | CFB8 (8-bit Cipher Feedback)          |
| 5                       | CFB128 (128-bit Cipher Feedback)      |
| 6                       | reserved                              |
| 7                       | reserved                              |

## Table 22.6-2. Working Status under DMA-AES Working mode

| AES_STATE_REG | Status   | Description                                       |
|---------------|----------|---------------------------------------------------|
| 0             | IDLE     | The AES accelerator is idle.                      |
| 1             | WORK     | The AES accelerator is in the middle of an operation. |
| 2             | DONE     | The AES accelerator completed operations.         |

## 22.6.1 Key, Plaintext, and Ciphertext

### Block Operation

During the block operations, the AES accelerator reads source data from DMA, and writes result data to DMA after the computation.

*   For encryption, DMA reads plaintext from memory, then passes it to AES as source data. After computation, AES passes ciphertext as result data back to DMA to write into memory.
*   For decryption, DMA reads ciphertext from memory, then passes it to AES as source data. After computation, AES passes plaintext as result data back to DMA to write into memory.

During block operations, the lengths of the source data and result data are the same. The total computation time is reduced because the DMA data operation and AES computation can happen concurrently.
```