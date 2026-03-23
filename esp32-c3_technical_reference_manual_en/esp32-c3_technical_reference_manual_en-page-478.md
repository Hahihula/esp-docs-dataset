

```markdown
| AES_STATE_REG[1:0] | Status | Description |
|--------------------|--------|-------------|
| 0                  | IDLE   | The AES accelerator is idle. |
| 1                  | WORK   | The AES accelerator is in the middle of an operation. |
| 2                  | DONE   | The AES accelerator completed operations. |

Table 18.5-2. Working Status under DMA-AES Working mode

Users can check the working status of the AES accelerator by inquiring the `AES_STATE_REG` register and comparing the return value against the Table 18.5-2 below.

When working in the DMA-AES working mode, the AES accelerator supports interrupt on the completion of computation. To enable this function, write 1 to the `AES_INT_ENA_REG` register. By default, the interrupt function is disabled. Also, note that the interrupt should be cleared by software after use.

## 18.5.1 Key, Plaintext, and Ciphertext

### Block Operation

During the block operations, the AES Accelerator reads source data from DMA, and write result data to DMA after the computation.

*   For encryption, DMA reads plaintext from memory, then passes it to AES as source data. After computation, AES passes ciphertext as result data back to DMA to write into memory.
*   For decryption, DMA reads ciphertext from memory, then passes it to AES as source data. After computation, AES passes plaintext as result data back to DMA to write into memory.

During block operations, the lengths of the source data and result data are the same. The total computation time is reduced because the DMA data operation and AES computation can happen concurrently.

The length of source data for AES Accelerator under DMA-AES working mode must be 128 bits or the integral multiples of 128 bits. Otherwise, trailing zeros will be added to the original source data, so the length of source data equals to the nearest integral multiples of 128 bits. Please see details in Table 18.5-3 below.

Table 18.5-3. TEXT-PADDING

```markdown
Function: TEXT-PADDING()

Input    : X, bit string.
Output   : Y = TEXT-PADDING(X), whose length is the nearest integral multiples of 128 bits.

Steps

Let us assume that X is a data-stream that can be split into n parts as following:
X = X₁||X₂||⋯||X_{n−1}||Xₙ
Here, the lengths of X₁,X₂,⋯,X_{n−1} all equal to 128 bits, and the length of Xₙ is t (0<=t<=127).

If t = 0, then
    TEXT-PADDING(X) = X;

If 0 < t <= 127, define a 128-bit block, X*_n*, and let X*_n* = Xₙ||0^{128−t}, then
    TEXT-PADDING(X) = X₁||X₂||⋯||X_{n−1}||X*_n* = X || 0^{128−t}
```