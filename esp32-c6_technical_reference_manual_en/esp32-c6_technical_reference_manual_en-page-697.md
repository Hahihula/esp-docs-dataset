

```markdown
4. Check the progress of the current message block.

* Poll register `SHA_BUSY_REG` until the content of this register becomes 0, indicating the accelerator has completed the calculation for the current message block and now is in the “idle” status³.

5. Decide if you have more message blocks to process:

* If yes, please go back to Step 2.
* Otherwise, please continue.

6. Obtain the message digest.

* Read the message digest from registers `SHA_H_n_REG`.

Note:
1. In this step, the software can also write the next message block (to be processed) in registers `SHA_M_n_REG`, if any, while the hardware starts SHA calculation, to save time.
2. You are resuming the SHA accelerator with the previously paused calculation.
3. Here you can decide if you want to insert other calculations. If yes, please go to the process for interleaved calculations for details.

As mentioned above, ESP32-C6 SHA accelerator supports “interleaving” calculation under the Typical SHA working mode.

The process to implement interleaved calculation is described below.

1. Prepare to hand the SHA accelerator over for an interleaved calculation by storing the following data of the previous calculation.

* The selected hash algorithm configured in the `SHA_MODE_REG` register.
* The message digest stored in registers `SHA_H_n_REG`.

2. Perform the interleaved calculation. For the detailed process of the interleaved calculation, please refer to Typical SHA process or DMA-SHA process, depending on the working mode of your interleaved calculation.

3. Prepare to hand the SHA accelerator back to the previously paused calculation by restoring the following data of the previous calculation.

* Write the previously stored hash algorithm back to register `SHA_MODE_REG`.
* Write the previously stored message digest back to registers `SHA_H_n_REG`.

4. Write the next message block from the previous paused calculation in registers `SHA_M_n_REG`, and set the `SHA_CONTINUE_REG` register to 1 to restart the SHA accelerator with the previously paused calculation.

23.4.2.2 DMA-SHA Mode Process

ESP32-C6 SHA accelerator does not support “interleaving” message digest calculation at the level of individual message blocks when using DMA, which means you cannot insert new calculation before a complete DMA-SHA process (of one or more message blocks) completes. In this case, users who need
```