**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**GoBack Link:** GoBack

---

**Table Header:**
Table 195-2. Working Status under DMA-AES Working mode

| AES_STATE_REG[1:0] | Status    | Description                    |
|--------------------|-----------|--------------------------------|
| 0                  | IDLE      | The AES accelerator is idle.   |
| 1                  | WORK      | The AES accelerator is in the middle of an operation. |
| 2                  | DONE      | The AES accelerator completed operations. |

**Body Text:**
When working in the DMA-AES working mode, the AES accelerator supports interrupt on the completion of computation. To enable this function, write 1 to the AES_INT_ENA_REG register. By default, the interrupt function is disabled. Also, note that the interrupt should be cleared by software after use.

**Subsection Title:**
19.5.1 Key, Plaintext, and Ciphertext

**Subsection Subtitle: Block Operation**

During block operations:

- For encryption, DMA reads plaintext from memory, then passes it to AES as source data. After computation, AES passes ciphertext as result data back to DMA to write into memory.
  
- For decryption, DMA reads ciphertext from memory, then passes it to AES as source data. After computation, AES passes plaintext as result data back to DMA to write into memory.

During block operations:

- The lengths of the source data and result data are the same. 
- Total computation time is reduced because the DMA data operation and AES computation can happen concurrently.
  
The length of source data for AES Accelerator under DMA-AES working mode must be 128 bits or the integral multiples of 128 bits.

**Table Title:**
Table 195-3. TEXT-PADDING

**Function Description (Text-Padding):**

**Function Name:** TEXT-PADDING()

**Input:** X, bit string.
  
**Output:** Y = TEXT-PADDING(X), whose length is the nearest integral multiples of 128 bits.

**Steps:**
Let us assume that X is a data-stream that can be split into n parts as follows:
X = X₁||X₂||...||Xₙ₋₁||Xₙ

Here, the lengths of X₁, X₂,..., Xₙ₋₁ all equal to 128 bits. The length of Xₙ is t (0<=t<=127).

If t = 0, then
TEXT-PADDING(X) = X;

If 0 < t <= 127, define a 128-bit block, Xₙ⁺, and let Xₙ⁺ = Xₙ||0^(128-t), then
TEXT-PADDING(X) = X₁||X₂||...||Xₙ₋₁||Xₙ⁺

**Subsection Title:**
19.5.2 Endianness

Under the DMA-AES working mode, the transmission of source data and result data for AES Accelerator is solely controlled by DMA. Therefore, the AES Accelerator cannot control the Endianness of the source data.

---

**Footer Information:** 
Espressif Systems
865 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback