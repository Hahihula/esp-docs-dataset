**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Body Text with Steps and Notes:**

(b) Set the SHA_START_REG register to 1 to start the SHA accelerator.

(c) Poll register SHA_BUY_REG until the content of this register becomes O, indicating the calculation of initial hash value is completed.

3. Process the current message block¹.
   - Write the message block in registers SHA_M_n_REG.

4. Start the SHA accelerator
   - Set the SHA_CONTINUE_REG register to 1. In this case, the accelerator uses the hash value stored in the SHA_H_n_REG register to start calculation.

5. Check the progress of the calculation.
   - Poll register SHA_BUY_REG until the content of this register becomes O, indicating the accelerator has completed the calculation for the current message block and now is in the “idle” status³.

6. Decide if you have more message blocks to process:
   - If yes, please go back to Step 3.
   - Otherwise, please continue.

7. Obtain the message digest
   - Read the message digest from registers SHA_H_n_REG.

**Note:**
1. In this step, the software can also write the next message block (to be processed) in registers SHA_M_n_REG if any, while the hardware starts SHA calculation to save time.
2. You are resuming the SHA accelerator with the previously paused calculation.
3. Here you can decide if you want to insert other calculations. If yes, please go to the process for interleaved calculations for details.

**Additional Information:**
As mentioned above, ESP32-S3 SHA accelerator supports “interleaving” calculation under the Typical SHA working mode.

The process to implement interleaved calculation is described below.
1. Prepare to hand the SHA accelerator over for an interleaved calculation by saving the following data of the previous calculation:
   - The selected hash algorithm stored in the SHA_MODE_REG register.
   - The message digest stored in registers SHA_H_n_REG.

2. Perform the interleaved calculation. For the detailed process of the interleaved calculation, please refer to Typical SHA process or DMA-SHA process, depending on the working mode of your interleaved calculation.

3. Prepare to hand the SHA accelerator back to the previously paused calculation by restoring the following data of the previous calculation.
   - Write the previously stored hash algorithm back to register SHA_MODE_REG
   - Write the previously stored message digest back to registers SHA_H_n_REG

**Footer:**
Espressif Systems  
848 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback