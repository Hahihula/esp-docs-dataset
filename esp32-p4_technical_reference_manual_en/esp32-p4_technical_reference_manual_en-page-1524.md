

```markdown
Chapter 31 ECDSA Digital Signature Peripheral (ECDSA_DS)

GoBack

31.5.1.1 IDLE Stage

In the IDLE stage:

1. Configure the static parameters including eFuse bits ECDSA_KEY, i.e., the value of private key d in ECDSA. To correctly configure the key value in eFuse, user need to write the key value in KEYn (n = 0 ~ 5), and set the corresponding EFUSE_KEY_PURPOSE_n as ECDSA_KEY. Please refer to Chapter 8 eFuse Controller (EFUSE) for more detailed configuration steps.

2. Configure the configuration register, including the following fields:
   (a) ECDSA_ECC_CURVE: Choose the elliptic curve of the ECDSA_DS module.
   (b) ECDSA_SOFTWARE_SET_Z: Choose to use direct input z.

3. Configure the register field ECDSA_START to enter the PREP stage.

31.5.1.2 PREP Stage

In the PREP stage, ECDSA_STATE_REG is BUSY, and the ECDSA_DS performs preparation.

Wait till the PREP stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA_DS will automatically enter the LOAD stage.

31.5.1.3 LOAD Stage

In the LOAD stage:

1. Provide input z into the ECDSA_DS using one of the following options:
   - Direct input z: write z to ECDSA_Z_MEM.
   - ECDSA_DS SHA interface: generate z from the message. For details, please refer to Section 31.5.1.6.

2. Provide signature and public key required by signature verification:
   (a) write signature (r, s) to ECDSA_R_MEM and ECDSA_S_MEM.
   (b) write public key (Qx, Qy) to ECDSA_QX_MEM and ECDSA_QY_MEM.

3. Write 1 to ECDSA_LOAD_DONE, indicating that the configuration is done. Then ECDSA_DS will automatically enter the PROC stage.

31.5.1.4 PROC Stage

In the PROC stage, ECDSA_STATE_REG is BUSY, and the ECDSA_DS performs ECDSA signature verification.

Wait till the PROC stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA_DS will automatically enter the POST stage.

31.5.1.5 POST Stage

In the POST stage, ECDSA_STATE_REG is BUSY, and the ECDSA_DS performs wrap-up work of the operation.

Wait till the POST stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA_DS will automatically return to the IDLE stage.
```