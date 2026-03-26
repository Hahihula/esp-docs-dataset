

```markdown
Chapter 25

AES Accelerator (AES)

25.1 Introduction

ESP32-P4 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software. The AES accelerator integrated in ESP32-P4 has two working modes, which are Typical AES and DMA-AES.

25.2 Features

The following functionality is supported:

*   Typical AES working mode
    -   AES-128/AES-256 encryption and decryption
*   DMA-AES working mode
    -   AES-128/AES-256 encryption and decryption
    -   Block cipher mode
        *   ECB (Electronic Codebook)
        *   CBC (Cipher Block Chaining)
        *   OFB (Output Feedback)
        *   CTR (Counter)
        *   CFB8 (8-bit Cipher Feedback)
        *   CFB128 (128-bit Cipher Feedback)
    -   GCM (Galois/Counter Mode)
    -   Interrupt on completion of computation

25.3 Clock and Reset

The AES accelerator is activated by setting the HP_SYS_CLKRST_CRYPTO_AES_CLK_EN bit in the HP_SYS_CLKRST_PERI_CLK_CTRL25_REG register and clearing the HP_SYS_CLKRST_RST_EN_AES bit in the HP_SYS_CLKRST_HP_RST_EN2_REG register. Besides, due to resource reuse between cryptography accelerator modules, users also need to additionally clear the HP_SYS_CLKRST_RST_EN_DS bit and the HP_SYS_CLKRST_RST_EN_KM bit in the HP_SYS_CLKRST_HP_RST_EN2_REG register.
```