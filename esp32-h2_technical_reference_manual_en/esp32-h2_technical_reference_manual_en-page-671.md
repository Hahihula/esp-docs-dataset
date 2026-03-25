

```markdown
Chapter 25 Elliptic Curve Digital Signature Algorithm (ECDSA)    GoBack

• Signature verification: POST stage


25.5.1.5 GAIN Stage

When the Signature Generation mode is selected, the ECDSA accelerator enters the GAIN stage after PROC stage:

1. Read data from the ECDSA memory:
   • read signature (r, s) from ECDSA_R_MEM and ECDSA_S_MEM.
   • read public key (Qx, Qy) from ECDSA_QX_MEM and ECDSA_QY_MEM.

2. Write 1 to ECDSA_GET_DONE, indicating the GAIN stage is done. Then the accelerator will automatically enter the POST stage.


25.5.1.6 POST Stage

In the POST stage, the ECDSA_STATE_REG is BUSY, and the ECDSA accelerator performs some wrap-up work of ECDSA operation.

1. Wait till the POST stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA accelerator will automatically return to the IDLE stage.


25.5.1.7 ECDSA SHA Interface

ESP32-H2’s ECDSA accelerator can automatically executes hash operation and generates z based on a direct input message.

For message hash, ECDSAS accelerator supports SHA algorithms SHA-224 (only valid when P-192 is selected as the elliptic curve) and SHA-256.

To use the ECDSA SHA interface, complete the following steps:

1. Pad the message by following the steps described in Section 25.4.2.3.
2. Parse the message and its padding into message blocks. See details in Section 25.4.2.4.
3. Process the current message block.
   • Write the current message block into ECDSA_MEM_M.

4. Start the ECDSA SHA interface¹.
   • If this is the first time to execute this step, write 1 to ECDSA_SHA_START to start the ECDSA SHA interface;
   • If this is not the first time to execute this step², write 1 to ECDSA_SHA_CONTINUE to continue the operation.

5. Check the progress of the current message block processing by polling.
   • Poll register ECDSA_SHA_BUSY until it’s IDLE, indicating the interface has completed the operation for the current message block.

6. Process the next message block:
   • If yes, go back to Step 3.
```