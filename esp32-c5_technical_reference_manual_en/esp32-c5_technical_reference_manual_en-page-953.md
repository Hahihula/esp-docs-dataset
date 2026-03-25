

```markdown
Chapter 28 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack


1. Read data from the ECDSA memory:
   - read signature (r, s) from ECDSA_MEM_R and ECDSA_MEM_S only in the Signature Generation mode.
   - read public key (Qx, Qy) from ECDSA_MEM_Qx and ECDSA_MEM_Qy both in the Signature Generation mode and the Public Key Export mode.

2. Write 1 to ECDSA_GET_DONE, indicating that the GAIN stage is done. Then the accelerator will automatically enter the POST stage.


28.5.1.6 POST Stage

In the POST stage, ECDSA_STATE_REG is BUSY, and the ECDSA accelerator performs some wrap-up work of ECDSA operation.

Wait till the POST stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA accelerator will automatically return to the IDLE stage.


28.5.1.7 ECDSA SHA Interface

ESP32-C5's ECDSA accelerator can automatically execute hash operation and generates z based on a direct input message.

For message hash, ECDSA accelerator supports SHA algorithms SHA-224 (only valid when P-192 is selected as the elliptic curve) and SHA-256.

To use the ECDSA SHA interface, complete the following steps:

1. Pad the message by following the steps described in Section 28.4.2.3.
2. Parse the message and its padding into message blocks. See details in Section 28.4.2.4.
3. Process the current message block.
   - Write the current message block into ECDSA_MEM_M.
4. Start the ECDSA SHA interface¹.
   - If this is the first time to execute this step, write 1 to ECDSA_SHA_START to start the ECDSA SHA interface;
   - If this is not the first time to execute this step², write 1 to ECDSA_SHA_CONTINUE to continue the operation.
5. Check the progress of the current message block processing by polling.
   - Poll register ECDSA_SHA_BUSY until it's IDLE, indicating that the interface has completed the operation for the current message block.
6. Process the next message block:
   - If there is message block to process, go back to Step 3.
   - If there is no more message blocks, exit.


Note:


Espressif Systems                           953
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```