

```markdown
11. Clear interrupt by writing 1 to the AES_INT_CLR_REG register, if any AES interrupt occurred during the computation.
12. Exit DMA by writing 1 to the AES_DMA_EXIT_REG register. After this, the content of the AES_STATE_REG becomes 0. Note that, you can exit DMA earlier, but only after Step 8 is completed.

## 25.7 GCM Algorithm

ESP32-P4's AES accelerator fully supports GCM Algorithm. In reality, the AAD, C and P that are longer than 2^32-1 bits are seldom used. Therefore, we specify that the length of AAD, C and P should be no longer than 2^32-1 here. Figure 25.7-1 below demonstrates how GCM encryption is implemented in the AES Accelerator of ESP32-P4.

![Figure 25.7-1. GCM Encryption Process](image_path_if_available)

GCM encryption is implemented as follows:

1. Hardware executes the ECB Algorithm to obtain the Hash subkey H, which is needed in the Hash computation.
2. Hardware executes the GHASH Algorithm to perform Hash computation with the padded AAD.

Figure 25.7-1. GCM Encryption Process
```