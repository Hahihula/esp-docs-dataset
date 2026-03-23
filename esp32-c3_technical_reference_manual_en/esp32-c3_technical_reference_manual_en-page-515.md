

```markdown
Note:
For more information about "message block", please refer to Section "2.1 Glossary of Terms and Acronyms" in FIPS PUB 180-4 Spec.
```

## 21.4.1.3 Setting the Initial Hash Value

Before hash task begins for any secure hash algorithms, the initial Hash value H(0) must be set based on different algorithms. However, the SHA accelerator uses the initial Hash values (constant C) stored in the hardware for hash tasks.

## 21.4.2 Hash Operation

After the preprocessing, the ESP32-C3 SHA accelerator starts to hash a message M and generates message digest of different lengths, depending on different hash algorithms. As described above, the ESP32-C3 SHA accelerator supports two working modes, which are Typical SHA and DMA-SHA. The operation process for the SHA accelerator under two working modes is described in the following subsections.

### 21.4.2.1 Typical SHA Mode Process

Usually, the SHA accelerator will process all blocks of a message and produce a message digest before starting the computation of the next message digest.

However, ESP32-C3 SHA also supports optional "interleaved" message digest calculation. Users can insert new calculation (both Typical SHA and DMA-SHA) each time the SHA accelerator completes a sequence of operations.

* In **Typical SHA** mode, this can be done after each individual message block.
* In **DMA-SHA** mode, this can be done after a full sequence of DMA operations is complete.

Specifically, users can read out the message digest from registers `SHA_H_n_REG` after completing part of a message digest calculation, and use the SHA accelerator for a different calculation. After the different calculation completes, users can restore the previous message digest to registers `SHA_H_n_REG`, and resume the accelerator with the previously paused calculation.

#### Typical SHA Process

1. Select a hash algorithm.
    * Configure the `SHA_MODE_REG` register based on Table 21.3-2.
2. Process the current message block¹.
    * Write the message block in registers `SHA_M_n_REG`.
3. Start the SHA accelerator.
    * If this is the first time to execute this step, set the `SHA_START_REG` register to 1 to start the SHA accelerator. In this case, the accelerator uses the initial hash value stored in hardware for a given algorithm configured in Step 1 to start the calculation;
```