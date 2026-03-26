

```markdown
6. Obtain the message digest:
    * Read the message digest from registers SHA_H_n_REG.

DMA-SHA process for SHA-512/t

1. Select a hash algorithm.
    * Select SHA-512/t algorithm by configuring the SHA_MODE_REG register to 7.

2. Configure the SHA_INT_ENA_REG register to enable or disable interrupt (Set 1 to enable).

3. Calculate the initial hash value.
    (a) Calculate t_string and t_length and initialize SHA_T_STRING_REG and SHA_T_LENGTH_REG with the generated t_string and t_length. For details, please refer to Section 29.4.1.3.
    (b) Set the SHA_START_REG register to 1 to start the SHA accelerator.
    (c) Poll register SHA_BUSY_REG until the content of this register becomes 0, indicating the calculation of initial hash value is completed.

4. Configure the number of message blocks.
    * Write the number of message blocks M to the SHA_DMA_BLOCK_NUM_REG register.

5. Start the DMA-SHA calculation.
    * Write 1 to register SHA_DMA_CONTINUE_REG to start the accelerator.

6. Wait till the completion of the DMA-SHA calculation, which happens when:
    * The content of SHA_BUSY_REG register becomes 0, or
        * An SHA interrupt occurs. In this case, please clear interrupt by writing 1 to the SHA_INT_CLEAR_REG register.

7. Obtain the message digest:
    * Read the message digest from registers SHA_H_n_REG.
```

## 29.4.3 Message Digest

After the hash task completes, the SHA accelerator writes the message digest from the task to registers `SHA_H_n_REG(n: 0 ~ 15)`. The lengths of the generated message digest are different depending on different hash algorithms. For details, see Table 29.4-4 below:
```