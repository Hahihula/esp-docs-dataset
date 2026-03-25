

```markdown
Chapter 19

AES Accelerator (AES)

19.1 Introduction

ESP32-H2 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software. The AES accelerator integrated in ESP32-H2 has two working modes, which are Typical AES and DMA-AES.

19.2 Features

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
    -   Interrupt on completion of computation

19.3 Clock and Reset

The AES accelerator is activated by setting the PCR_AES_CLK_EN bit and clearing the PCR_AES_RST_EN bit in the PCR_AES_CONF_REG register. Besides, due to resource reuse between cryptography accelerator modules, users also need to additionally clear the PCR_DS_RST_EN bit in the PCR_DS_CONF_REG register.
```