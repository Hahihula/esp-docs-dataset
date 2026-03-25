

```markdown
Chapter 22 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack

1. Configure the static parameters including eFuse bits:
   (a) ECDSA_KEY: The value of private key d in ECDSA. To correctly configure the key value in eFuse, users need to write the key value in KEYn (n = 0-5), and set the corresponding EFUSE_KEY_PURPOSE_n as ECDSA_KEY. Please refer to Chapter 5 eFuse Controller (EFUSE) for more detailed configuration steps.

2. Configure ECDSA_CONF_REG, including the following fields:
   (a) ECDSA_WORK_MODE: Select the working mode of the ECDSA accelerator.
   (b) ECDSA_ECC_CURVE: Select the elliptic curve of the ECDSA accelerator.
   (c) ECDSA_SOFTWARE_SET_Z: Configure whether to use direct input z.
   (d) ECDSA_DETERMINISTIC_K: Configure whether to use deterministic k.
   (e) ECDSA_DETERMINISTIC_LOOP: Configure the loop number of deterministic k.

3. Configure the register field ECDSA_START to enter the PREP stage.

Note:
For more details about Deterministic ECDSA, please refer to RFC6979.

22.5.1.2 PREP Stage

In the PREP stage, ECDSA_STATE_REG is BUSY, and the ECDSA accelerator performs preparation.

Wait till the PREP stage to end by polling ECDSA_BUSY until it is not BUSY. Then the ECDSA accelerator will automatically enter the LOAD stage.

22.5.1.3 LOAD Stage

In the LOAD stage:

1. Provide input z into the ECDSA accelerator using one of the following options:
   - Direct input z: write z to ECDSA_MEM_Z.
   - ECDSA SHA interface: generate z from the message. For details, please refer to Section 22.5.1.7.

2. According to the selected ECDSA_WORK_MODE, configure as follows:
   - Signature Verification:
     (a) write signature (r, s) to ECDSA_MEM_R and ECDSA_MEM_S.
     (b) write public key (Qx, Qy) to ECDSA_MEM_Qx and ECDSA_MEM_Qy.
   - Signature Generation:
     (a) no other configuration is required.
   - Public Key Export:
     (a) no other configuration is required.

3. Write 1 to ECDSA_LOAD_DONE, indicating that the configuration is done. Then the accelerator will automatically enter the PROC stage.
```