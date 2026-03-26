

```markdown
## 29.4.2 Hash Operation

After the preprocessing, the ESP32-P4 SHA accelerator starts to hash a message M and generates message digest of different lengths, depending on different hash algorithms. As described above, the ESP32-P4 SHA accelerator supports two working modes, which are **Typical SHA** and DMA-SHA. The operation process for the SHA accelerator under two working modes is described in the following subsections.

### 29.4.2.1 Typical SHA Mode Process

Usually, the SHA accelerator will process all blocks of a message and produce a message digest before starting the computation of the next message digest.

However, ESP32-P4 SHA also supports optional "interleaved" message digest calculation in Typical SHA mode, which means before SHA completes all blocks of the current message, users are given a chance to insert new computation of another message digest upon the completion of each individual block of the current message.

Specifically, users can read out the message digest from registers `SHA_H_n_REG` after completing part of a message digest calculation, and use the SHA accelerator for a different calculation. After the different calculation completes, users can restore the previous message digest to registers `SHA_H_n_REG`, and resume the accelerator with the previously paused calculation.

#### Typical SHA Process (except for SHA-512/t)

1. Select a hash algorithm.
   - Configure the `SHA_MODE_REG` register based on Table 29.3-2.
2. Process the current message block.
   - Write the message block in registers `SHA_M_n_REG`.
3. Start the SHA accelerator¹.
   - If this is the first time to execute this step, set the `SHA_START_REG` register to 1 to start the SHA accelerator. In this case, the accelerator uses the initial hash value stored in hardware for a given algorithm configured in Step 1 to start the calculation;
   - If this is not the first time to execute this step², set the `SHA_CONTINUE_REG` register to 1 to start the SHA accelerator. In this case, the accelerator uses the hash value stored in the `SHA_H_n_REG` register to start calculation.
4. Check the progress of the current message block.
   - Poll register `SHA_BUSY_REG` until the content of this register becomes 0, indicating the accelerator has completed the calculation for the current message block and now is in the "idle" status³.
5. Decide if you have more message blocks to process:
   - If yes, please go back to Step 2.
   - Otherwise, please continue.
6. Obtain the message digest.
   - Read the message digest from registers `SHA_H_n_REG`.
```