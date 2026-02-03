**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Section Header:**
18.4.2.1 Typical SHA Mode Process

**Body Text:**
Usually, the SHA accelerator will process all blocks of a message and produce a message digest before starting the next message digest.

However, ESP32-S3 SHA working in Typical SHA mode also supports optional “interleaved” message digest calculation. Users can insert new calculation (both Typical SHA and DMA-SHA) each time the SHA accelerator completes one message block. To be more specific, users can store the message digest in registers SHA_H_n_REG after completing each message block, and assign the accelerator with other higher priority tasks. After the inserted calculation completes, users can put the message digest stored back to registers SHA_H_n_REG, and resume the accelerator with the previously paused calculation.

**Subsection Title:**
Typical SHA Process (except for SHA-512/t)

**List Items in Subsection:**
1. Select a hash algorithm.
   - Configure the SHA_MODE_REG register based on Table 18.3-2
2. Process the current message block ¹.
   - Write the message block in registers SHA_M_n_REG.
3. Start the SHA accelerator.
   - If this is the first time to execute this step, set the SHA_START_REG register to 1 to start the SHA accelerator. In this case, the accelerator uses the initial hash value stored in hardware for a given algorithm configured in Step 1 to start the calculation;
   - If this is not the first time to execute this step², set the SHA_CONTINUE_REG register to 1 to start the SHA accelerator. In this case, the accelerator uses the hash value stored in the SHA_H_n_REG register to start calculation.
4. Check the progress of the current message block.
   - Poll register SHA_BUSY_REG until the content of this register becomes O, indicating the accelerator has completed the calculation for the current message block and now is in the “idle” status ³.
5. Decide if you have more message blocks to process:
   - If yes, please go back to Step 2.
   - Otherwise, please continue.
6. Obtain the message digest from registers SHA_H_n_REG.

**Subsection Title:**
Typical SHA Process (SHA-512/t)

**List Items in Subsection:**
1. Select a hash algorithm.
2. Calculate the initial hash value.
   - Configure the SHA_MODE_REG register to 7 for SHA-512/t.
   - Calculate t_string and t_length and initialize SHA_T_STRING_REG and SHA_T_LENGTH_REG with the generated t_string and t_length. For details, please refer to Section 18.4.1.3.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** 
847 ESP32-S3 TRM (Version 1.7)