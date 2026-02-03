**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Section Heading and Content:**

4. **Instruction:** Write the next message block from the previous paused calculation in registers `SHA_M_n_REG`, and set the `SHA_CONTINUE_REG` register to 1 to restart the SHA accelerator with previously paused calculation.

---

**Subsection Title:**
18.4.2.2 DMA-SHA Mode Process

**Body Text:**  
ESP32-S3 SHA accelerator does not support “interleaving” message digest calculation when using the DMA, which means you cannot insert new calculation before the whole DMA-SHA process completes. In this case, users who need inserted calculation are recommended to divide your message blocks and perform several DMA-SHA calculations instead of trying to compute all messages in one go.

In contrast to the Typical SHA working mode, where the SHA accelerator is working under the DMA-SHA mode, all data read are completed via DMA.

Therefore, users are required to configure the DMA controller following the description in Chapter 3 GDMA Controller (GDMA).

**Subsection Title:**
DMA-SHA process (except SHA-512/t)

**List of Steps:**  
1. **Instruction:** Select a hash algorithm.
   - **Detail:** Select a hash algorithm by configuring the `SHA_MODE_REG` register. For details, please refer to Table 18.3-2.

2. **Instruction:** Configure the `SHA_INT_ENA_REG` register to enable or disable interrupt (Set 1 to enable).

3. **Instruction:** Configure the number of message blocks.
   - Write the number of message blocks M to the `SHA_DMA_BLOCK_NUM_REG` register.

4. **Instruction:** Start the DMA-SHA calculation.
   - If the current DMA-SHA calculation follows a previous calculation, firstly write the message digest from the previous calculation to registers `SHA_H_n_REG`, then write 1 to register `SHA_DMA_CONTINUE_REG` to start SHA accelerator;
   - Otherwise, write 1 to register `SHA_DMA_START_REG` to start the accelerator.

5. **Instruction:** Wait till completion of the DMA-SHA calculation, which happens when:
   - The content of `SHA_BUY_REG` register becomes 0,
   - An SHA interrupt occurs. In this case, please clear interrupt by writing 1 to the `SHA_INT_CLEAR_REG` register.
   
6. **Instruction:** Obtain the message digest:  
   - Read the message digest from registers `SHA_H_n_REG`.

**Subsection Title:**
DMA-SHA process for SHA-512/t

**List of Steps:**  
1. Select a hash algorithm.

2. **Instruction:** Configure the `SHA_MODE_REG` register to 7.
   
3. **Instruction:** Configure the `SHA_INT_ENA_REG` register to enable or disable interrupt (Set 1 to enable).

4. Calculate the initial hash value.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Information:**
ESP32-S3 TRM (Version 1.7)