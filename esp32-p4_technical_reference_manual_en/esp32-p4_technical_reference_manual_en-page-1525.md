

```markdown
## 31.5.1.6 ECDSA_DS SHA Interface

ESP32-P4's ECDSA_DS module can automatically execute hash operation and generates z based on a direct input message.

For message hash, the ECDSA_DS module supports SHA algorithms SHA-224 (only valid when P-192 is selected as the elliptic curve) and SHA-256.

To use the ECDSA_DS SHA interface, complete the following steps:

1. Pad the message by following the steps described in Section 31.4.2.3.
2. Parse the message and its padding into message blocks. See details in Section 31.4.2.4.
3. Process the current message block.

    * Write the current message block into `ECDSA_MEM_M`.

4. Start the ECDSA_DS SHA interface¹.

    * If this is the first time to execute this step, write 1 to `ECDSA_SHA_START` to start the ECDSA_DS SHA interface;
    * If this is not the first time to execute this step², write 1 to `ECDSA_SHA_CONTINUE` to continue the operation.

5. Check the progress of the current message block processing by polling.

    * Poll register `ECDSA_SHA_BUSY` until it's IDLE, indicating that the interface has completed the operation for the current message block.

6. Process the next message block:

    * If there is message block to process, go back to Step 3.
    * If there is no more message blocks, exit.

**Note:**

1. In this step, the software can also write the next message block to be processed, if any, in register `ECDSA_MEM_M`, while the interface starts SHA operation, to save time.
2. You are resuming the ECDSA_DS SHA interface with the previously paused operation.

## 31.5.2 Clocks and Resets

ESP32-P4's ECDSA_DS module has one clock module and one reset module. It is activated by setting the `HP_SYS_CLKRST_REG_CRYPTO_ECDSA_CLK_EN` bit in the `HP_SYS_CLKRST_PERI_CLK_CTRL25_REG` register and clearing the `HP_SYS_CLKRST_REG_RST_EN_ECDSA` bit in the `HP_SYS_CLKRST_HP_RST_EN2_REG` register. For details on how to configure the ECDSA_DS clock and reset, please refer to Chapter 10 Reset and Clock.

## 31.5.3 Interrupts

ESP32-P4's ECDSA_DS module can generate the interrupt signal `ECDSA_INTR` and send it to Interrupt Matrix.
```