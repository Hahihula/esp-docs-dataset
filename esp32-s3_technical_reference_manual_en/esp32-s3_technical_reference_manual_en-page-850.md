**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Body Text with Instructions and Steps:**

(a) Calculate t_string and t_length and initialize SHA_T_STRING_REG and SHA_T_LENGTH_REG with the generated t_string and t_length. For details, please refer to Section 18.4.1.3.

(b) Set the SHA_START_REG register to 1 to start the SHA accelerator.

(c) Poll register SHA_BUSY_REG until the content of this register becomes 0, indicating the calculation of initial hash value is completed.

**Step-by-step Instructions:**

- Configure the number of message blocks.
  - Write the number of message blocks M to the SHA_DMA_BLOCK_NUM_REG register.

- Start the DMA-SHA calculation.
  - Write 1 to register SHA_DMA_CONTINUE_REG to start the accelerator.

- Wait till the completion of the DMA-SHA calculation, which happens when:
  - The content of SHA BUSY_REG register becomes 0,
    - An SHA interrupt occurs. In this case, please clear interrupt by writing 1 to the SHA_INT_CLEAR_REG register.
  
**Step-by-step Instructions:**

- Obtain the message digest from registers SHA_H_n_REG.

**Subsection Title and Description:**
18.4.3 Message Digest

After the hash task completes, the SHA accelerator writes the message digest from the task to registers SHA_H_n_REG(n): 0~15). The lengths of the generated message digest are different depending on different hash algorithms. For details, see Table 18.4-4 below:

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)