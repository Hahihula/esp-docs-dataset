**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**Section Titles and Content:**

### **19.4.3 Operation Process**

#### Single Operation

1. Write O to the `AES_DMA_ENABLE_REG` register.
2. Initialize registers `AES_MODE_REG`, `AES_KEY_n_REG`, `AES_TEXT_IN_m_REG`.
3. Start operation by writing 1 to the `AES_TRIGGER_REG` register.
4. Wait till the content of the `AES_STATE_REG` register becomes O, which indicates the operation is completed.
5. Read results from the `AES_TEXT_OUT_m_REG` register.

#### Consecutive Operations

In consecutive operations, primarily the input `AES_TEXT_IN_m_REG` and output `AES_TEXT_OUT_m_REG` registers are being written and read, while the content of `AES_DMA_ENABLE_REG`, `AES_MODE_REG`, `AES_KEY_n_REG` is kept unchanged. Therefore, the initialization can be simplified during the consecutive operation.

1. Write O to the `AES_DMA_ENABLE_REG` register before starting the first operation.
2. Initialize registers `AES_MODE_REG` and `AES_KEY_n_REG` before starting the first operation.
3. Update the content of `AES_TEXT_IN_m_REG`.
4. Start operation by writing 1 to the `AES_TRIGGER_REG` register.
5. Wait till the content of the `AES_STATE_REG` register becomes O, which indicates the operation completes.
6. Read results from the `AES_TEXT_OUT_m_REG` register, and return to Step 3 to continue the next operation.

### **19.5 DMA-AES Working Mode**

In the DMA-AES working mode, the AES accelerator supports six block cipher modes including ECB/CBC/CFB/CTR/CFB8/CFB128. Users can choose the block cipher mode by configuring the `AES_BLOCK_MODE_REG` register according to Table 19.5-1 below.

**Table Title:**
Table 19.5-1. Block Cipher Mode

| AES_BLOCK_MODE_REG[2:0] | Block Cipher Mode |
|-------------------------|--------------------|
| O                       | ECB (Electronic Codebook) |
| 1                       | CBC (Cipher Block Chaining) |
| 2                       | OFB (Output Feedback)    |
| 3                       | CTR (Counter)          |
| 4                       | CFB8 (8-bit Cipher Feedback) |
| 5                       | CFB128 (128-bit Cipher Feedback) |
| 6                       | reserved              |
| 7                       | reserved              |

**Footer:**
Espressif Systems
Page number: 863

**Document Information:** 
ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
- GoBack