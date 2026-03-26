

```markdown
Chapter 29 SHA Accelerator (SHA)

Typical SHA Process (SHA-512/t)

1. Select a hash algorithm.
   - Configure the `SHA_MODE_REG` register to 7 for SHA-512/t.

2. Calculate the initial hash value.
   (a) Calculate t_stiring and t_length and initialize `SHA_T_STRING_REG` and `SHA_T_LENGTH_REG` with the generated t_string and t_length. For details, please refer to Section 29.4.1.3.
   (b) Set the `SHA_START_REG` register to 1 to start the SHA accelerator.
   (c) Poll register `SHA_BUSY_REG` until the content of this register becomes 0, indicating the calculation of initial hash value is completed.

3. Process the current message block¹.
   - Write the message block in registers `SHA_M_n_REG`.

4. Start the SHA accelerator
   - Set the `SHA_CONTINUE_REG` register to 1. In this case, the accelerator uses the hash value stored in the `SHA_H_n_REG` register to start calculation.

5. Check the progress of the calculation.
   - Poll register `SHA_BUSY_REG` until the content of this register becomes 0, indicating the accelerator has completed the calculation for the current message block and now is in the “idle” status³.

6. Decide if you have more message blocks to process:
   - If yes, please go back to Step 3.
   - Otherwise, please continue.

7. Obtain the message digest.
   - Read the message digest from registers `SHA_H_n_REG`.

Note:

1. In this step, the software can also write the next message block (to be processed) in registers `SHA_M_n_REG`, if any, while the hardware starts SHA calculation, to save time.

2. You are resuming the SHA accelerator with the previously paused calculation.

3. Here you can decide if you want to insert other calculations. If yes, please go to the process for interleaved calculations for details.
```
As mentioned above, ESP32-P4 SHA accelerator supports “interleaving” calculation under the Typical SHA working mode.

The process to implement interleaved calculation is described below.

1. Prepare to hand the SHA accelerator over for an interleaved calculation by storing the following data of the previous calculation.
   - The selected hash algorithm configured in the `SHA_MODE_REG` register.
   - The message digest stored in registers `SHA_H_n_REG`.
```