

```markdown
2. Perform the interleaved calculation. For the detailed process of the interleaved calculation, please refer to Typical SHA process or DMA-SHA process, depending on the working mode of your interleaved calculation.
3. Prepare to hand the SHA accelerator back to the previously paused calculation by restoring the following data of the previous calculation.

  * Write the previously stored hash algorithm back to register SHA_MODE_REG.
  * Write the previously stored message digest back to registers SHA_H_n_REG.

4. Write the next message block from the previous paused calculation in registers SHA_M_n_REG, and set the SHA_CONTINUE_REG register to 1 to restart the SHA accelerator with the previously paused calculation.

29.4.2.2 DMA-SHA Mode Process

ESP32-P4 SHA accelerator does not support “interleaving” message digest calculation at the level of individual message blocks when using DMA, which means you cannot insert new calculation before a complete DMA-SHA process (of one or more message blocks) completes. In this case, users who need interleaved operation are recommended to divide the message blocks and perform several DMA-SHA calculations, instead of trying to compute all the messages in one go.

Single DMA-SHA calculation supports up to 63 message blocks.

In contrast to the Typical SHA working mode, when the SHA accelerator is working under the DMA-SHA mode, all data read are completed via GDMA-AXI. Therefore, users are required to configure the GDMA-AXI controller following the description in Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI).

DMA-SHA process (except SHA-512/t)

1. Select a hash algorithm.

  * Select a hash algorithm by configuring the SHA_MODE_REG register. For details, please refer to Table 29.3-2.
2. Configure the SHA_INT_ENA_REG register to enable or disable interrupt (Set 1 to enable).
3. Configure the number of message blocks.

  * Write the number of message blocks M to the SHA_DMA_BLOCK_NUM_REG register.
4. Start the DMA-SHA calculation.

  * If the current DMA-SHA calculation follows a previous calculation, firstly write the message digest from the previous calculation to registers SHA_H_n_REG, then write 1 to register SHA_DMA_CONTINUE_REG to start SHA accelerator;
  * Otherwise, write 1 to register SHA_DMA_START_REG to start the accelerator.
5. Wait till the completion of the DMA-SHA calculation, which happens when:

  * The content of SHA_BUSY_REG register becomes 0, or
  * An SHA interrupt occurs. In this case, please clear interrupt by writing 1 to the SHA_INT_CLEAR_REG register.
```