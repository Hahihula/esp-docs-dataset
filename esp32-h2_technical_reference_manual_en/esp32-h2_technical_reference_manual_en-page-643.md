

```markdown
M₀⁽ⁱ⁾, the next 32 bits are M₁⁽ⁱ⁾, and so on up to M₁₅⁽ⁱ⁾.

During the task, all the message blocks are written into the SHA_M_n_REG: M₀⁽ⁱ⁾ is stored in SHA_M_O_REG, M₁⁽ⁱ⁾ stored in SHA_M_1_REG, ..., and M₁₅⁽ⁱ⁾ stored in SHA_M_15_REG.


Note:

For more information about "message block", please refer to FIPS PUB 180-4 Spec > Section "Glossary of Terms and Acronyms".

23.4.1.3 Setting the Initial Hash Value

Before hash operation begins for any secure hash algorithms, the initial Hash value H⁽⁰⁾ must be set based on different algorithms. However, the SHA accelerator uses the initial Hash values (constant C) stored in the hardware for hash tasks.

23.4.2 Hash Operation

After the preprocessing, the ESP32-H2 SHA accelerator starts to hash a message M and generates message digest of different lengths, depending on different hash algorithms. As described above, the ESP32-H2 SHA accelerator supports two working modes, which are Typical SHA and DMA-SHA. The operation process for the SHA accelerator under two working modes is described in the following subsections.

23.4.2.1 Typical SHA Mode Process

Usually, the SHA accelerator will process all blocks of a message and produce a message digest before starting the computation of the next message digest.

However, ESP32-H2 SHA also supports optional "interleaved" message digest calculation in Typical SHA mode, which means before SHA completes all blocks of the current message, users are given a chance to insert new computation of another message digest upon the completion of each individual block of the current message.

Specifically, users can read out the message digest from registers SHA_H_n_REG after completing part of a message digest calculation, and use the SHA accelerator for a different calculation. After the different calculation completes, users can restore the previous message digest to registers SHA_H_n_REG, and resume the accelerator with the previously paused calculation.

Typical SHA Process

1. Select a hash algorithm.
   - Configure the SHA_MODE_REG register based on Table 23.3-2.
2. Process the current message block.
   - Write the message block in registers SHA_M_n_REG.
3. Start the SHA accelerator¹.
   - If this is the first time to execute this step, set the SHA_START_REG register to 1 to start the SHA accelerator. In this case, the accelerator uses the initial hash value stored in hardware for a given algorithm configured in Step 1 to start the calculation;
```