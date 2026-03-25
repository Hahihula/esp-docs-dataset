

```markdown
Chapter 28 Elliptic Curve Digital Signature Algorithm (ECDSA)    GoBack


Figure 28.5-1. ECDSA Process



The detailed programming procedures of each stage are described in the following sections.



28.5.1.1 IDLE Stage



In the IDLE stage:



1. Configure the static parameters including eFuse bits:

   (a) ECDSA_KEY: The value of private key d in ECDSA. To correctly configure the key value in eFuse, users need to write the key value in KEYn (n = 0-5), and set the corresponding EFUSE_KEY_PURPOSE_n as ECDSA_KEY. Please refer to Chapter 7 eFuse Controller (EFUSE) for more detailed configuration steps.

2. Configure ECDSA_CONF_REG, including the following fields:

   (a) ECDSA_WORK_MODE: Select the working mode of the ECDSA accelerator.
   
   (b) ECDSA_ECC_CURVE: Select the elliptic curve of the ECDSA accelerator.
   
   (c) ECDSA_SOFTWARE_SET_Z: Configure whether to use direct input z.
   
   (d) ECDSA_DETERMINISTIC_K: Configure whether to use deterministic k.

3. Configure the register field ECDSA_START to enter the PREP stage.



Espressif Systems    951    ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```