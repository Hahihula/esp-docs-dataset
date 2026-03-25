

```markdown
Notice:
ESP32-C5's Digital Signature Algorithm (DSA) module will call the AES accelerator. Therefore, users cannot access the AES accelerator when Digital Signature Algorithm (DSA) module is working.
```

## 22.5 Typical AES Working Mode

In the Typical AES working mode, users can check the working status of the AES accelerator by inquiring the `AES_STATE_REG` register and comparing the return value against the Table 22.5-1 below.

Table 22.5-1. Working Status under Typical AES Working Mode

| AES_STATE_REG | Status   | Description                                                                 |
|---------------|----------|-----------------------------------------------------------------------------|
| 0             | IDLE     | The AES accelerator is idle or completed operation.                         |
| 1             | WORK     | The AES accelerator is in the middle of an operation.                       |

### 22.5.1 Key, Plaintext, and Ciphertext

The encryption or decryption key is stored in `AES_KEY_n_REG`, which is a set of eight 32-bit registers.

*   For AES-128 encryption or decryption, the 128-bit key is stored in `AES_KEY_0_REG ~ AES_KEY_3_REG`.
*   For AES-256 encryption or decryption, the 256-bit key is stored in `AES_KEY_0_REG ~ AES_KEY_7_REG`.

The plaintext and ciphertext are stored in `AES_TEXT_IN_m_REG` and `AES_TEXT_OUT_m_REG`, which are two sets of four 32-bit registers.

*   For AES-128 or AES-256 encryption, the `AES_TEXT_IN_m_REG` registers are initialized with plaintext. Then, the AES accelerator stores the ciphertext into `AES_TEXT_OUT_m_REG` after operation.
*   For AES-128 or AES-256 decryption, the `AES_TEXT_IN_m_REG` registers are initialized with ciphertext. Then, the AES accelerator stores the plaintext into `AES_TEXT_OUT_m_REG` after operation.
```