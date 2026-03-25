

```markdown
Note:
For more details about Deterministic ECDSA, please refer to RFC6979.
```

## 28.5.1.2 PREP Stage

In the PREP stage, `ECDSA_STATE_REG` is BUSY, and the ECDSA accelerator performs preparation.

Wait till the PREP stage to end by polling `ECDSA_BUSY` until it is not BUSY. Then the ECDSA accelerator will automatically enter the LOAD stage.

## 28.5.1.3 LOAD Stage

In the LOAD stage:

1. Provide input z into the ECDSA accelerator using one of the following options:
   - Direct input z: write z to `ECDSA_MEM_Z`.
   - ECDSA SHA interface: generate z from the message. For details, please refer to Section 28.5.1.7.

2. According to the selected `ECDSA_WORK_MODE`, configure as follows:

   - Signature Verification:
     - (a) write signature `(r, s)` to `ECDSA_MEM_R` and `ECDSA_MEM_S`.
     - (b) write public key `(Qx, Qy)` to `ECDSA_MEM_Qx` and `ECDSA_MEM_Qy`.

   - Signature Generation: no other configuration is required.

   - Public Key Export: no other configuration is required.

3. Write 1 to `ECDSA_LOAD_DONE`, indicating that the configuration is done. Then the accelerator will automatically enter the PROC stage.

## 28.5.1.4 PROC Stage

In the PROC stage, `ECDSA_STATE_REG` is BUSY, and the ECDSA accelerator performs ECDSA operation based on the selected working mode.

Wait till the PROC stage to end by polling `ECDSA_BUSY` until it is not BUSY. Then the ECDSA accelerator will automatically enter the either the GAIN stage or the POST stage depending on the selected working mode:

- Signature generation: GAIN stage
- Signature verification: POST stage

## 28.5.1.5 GAIN Stage

When the Signature Generation mode or the Public Key Export mode is selected, the ECDSA accelerator enters the GAIN stage after PROC stage:
```