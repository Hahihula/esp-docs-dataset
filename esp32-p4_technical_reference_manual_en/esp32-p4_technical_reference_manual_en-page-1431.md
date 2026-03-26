

```markdown
Chapter 25 AES Accelerator (AES)
GoBack

25.5.3 Operation Process

Single Operation

1. Write 0 to the `AES_DMA_ENABLE_REG` register.
2. Initialize registers `AES_MODE_REG`, `AES_KEY_n_REG`, and `AES_TEXT_IN_m_REG`.
3. Start operation by writing 1 to the `AES_TRIGGER_REG` register.
4. Wait till the content of the `AES_STATE_REG` register becomes 0, which indicates the operation is completed.
5. Read results from the `AES_TEXT_OUT_m_REG` register.

Consecutive Operations

In consecutive operations, primarily the input `AES_TEXT_IN_m_REG` and output `AES_TEXT_OUT_m_REG` registers (m: 0-3) are being written and read, while the content of `AES_DMA_ENABLE_REG`, `AES_MODE_REG`, and `AES_KEY_n_REG` is kept unchanged. Therefore, the initialization can be simplified during the consecutive operation.

1. Write 0 to the `AES_DMA_ENABLE_REG` register before starting the first operation.
2. Initialize registers `AES_MODE_REG` and `AES_KEY_n_REG` before starting the first operation.
3. Update the content of `AES_TEXT_IN_m_REG`.
4. Start operation by writing 1 to the `AES_TRIGGER_REG` register.
5. Wait till the content of the `AES_STATE_REG` register becomes 0, which indicates the operation completes.
6. Read results from the `AES_TEXT_OUT_m_REG` register, and return to Step 3 to continue the next operation.
```