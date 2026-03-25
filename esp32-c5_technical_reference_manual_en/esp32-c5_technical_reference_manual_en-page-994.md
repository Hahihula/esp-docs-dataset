

```markdown
Chapter 31 Key Manager

Figure 31.6-1. AES Deploy Mode

Detailed Process

1. Generate locally k1, k2, and init_key.
2. Calculate locally k1_encrypted and k2_info.
3. Then complete the key deployment in Key Manager:
   (a) Write init_key into either a eFuse block with purpose of EFUSE_KM_INIT_KEY or sw_init_key, depending on your need.
   (b) Write k2_info and k1_encrypted into internal memory of the Key Manager.
   (c) Wait for the Key Manager to complete the deployment.
   (d) Read key_info from the internal memory of the Key Manager by specifying the address.

Notes:

• Due to the necessity of re-deploying the key each time when the chip powers up, if key_info is to be used for key recovery upon the next power-up, ensure that key_info must persist after the chip powers off. A common method is to store it in the flash.
• AES Deploy Mode is suitable for factory production: the manufacturer provides the factory with init_key and the firmware encrypted with k1, and store k2_info and k1_encrypted in the firmware.
   – In this case, it is recommended to include a private key first-time deployment process in the firmware, to store key_info. In the subsequent chip power-ups, use the recovery deployment mode, instead of deploying via AES mode each time. This helps effectively defend against eFuse slice attacks.
```