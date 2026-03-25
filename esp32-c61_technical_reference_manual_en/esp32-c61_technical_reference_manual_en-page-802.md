

```markdown
Chapter 22 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack


22.5.1.4 PROC Stage

In the PROC stage, ECDSA_STATE_REG is BUSY, and the ECDSA accelerator performs ECDSA operation based on the selected working mode.

Wait till the PROC stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA accelerator will automatically enter the either the GAIN stage or the POST stage depending on the selected working mode:

- Signature generation: GAIN stage
- Signature verification: POST stage


22.5.1.5 GAIN Stage

When the Signature Generation mode or the Public Key Export mode is selected, the ECDSA accelerator enters the GAIN stage after PROC stage:

1. Read data from the ECDSA memory:
   - read signature (r, s) from ECDSA_MEM_R and ECDSA_MEM_S only in the Signature Generation mode.
   - read public key (Qx, Qy) from ECDSA_MEM_Qx and ECDSA_MEM_Qy both in the Signature Generation mode and the Public Key Export mode.

2. Write 1 to ECDSA_GET_DONE, indicating that the GAIN stage is done. Then the accelerator will automatically enter the POST stage.


22.5.1.6 POST Stage

In the POST stage, ECDSA_STATE_REG is BUSY, and the ECDSA accelerator performs some wrap-up work of ECDSA operation.

Wait till the POST stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA accelerator will automatically return to the IDLE stage.


22.5.1.7 ECDSA SHA Interface

ESP32-C61’s ECDSA accelerator can automatically execute hash operation and generates z based on a direct input message.

For message hash, ECDSA accelerator supports SHA algorithms SHA-224 (only valid when P-192 is selected as the elliptic curve) and SHA-256.

To use the ECDSA SHA interface, complete the following steps:

1. Pad the message by following the steps described in Section 22.4.2.3.
2. Parse the message and its padding into message blocks. See details in Section 22.4.2.4.
3. Process the current message block.
   - Write the current message block into ECDSA_MEM_M.
4. Start the ECDSA SHA interface¹.
```