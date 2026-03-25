

```markdown
(b) Write k1 * G and k2_info to the internal memory of the Key Manager.
(c) Wait for the Key Manager to complete the deployment.
(d) Read k2 * G and key_info (corresponding to the negotiated private key k1 * k2 * G) from the internal memory of the Key Manager by specifying the address.

Notes:

* ECDH1 Deploy Mode is suitable for factory production: the manufacturer provides the factory with init_key and the firmware encrypted with k1 * k2 * G, and store k2_info and k1 * G in the firmware.
  - In this case, it is recommended to include a private key first-time deployment process in the firmware, to store key_info. In the subsequent chip power-ups, use the recovery deployment mode, instead of deploying via ECDH1 mode each time. This helps effectively defend against eFuse slice attacks.
  - Note that this deployment method requires a trusted factory, as the factory will have access to the plaintext init_key (used to be burned into eFuse). If the factory is untrusted and knows how to use init_key to decrypt k2_info into k2, it may result in a potential leakage of k1 * k2 * G.

* Similar to AES Delpy Mode, when using ECDH1 Deploy Mode to deploy the key each time, it is essential to ensure that the values of init_key, k2_info, and k1 * G are not leaked simultaneously.
  - If using init_key stored in a eFuse block with purpose of EFUSE_KM_INIT_KEY, k2_info and k1 * G may be transmitted in an untrusted environment. However, this requires to locally retain the init_key that was written to the EFUSE_KM_INIT_KEY eFuse block at the first time.
  - If using sw_init_key, the transmission of sw_init_key, k2_info, and k1 * G must occur in a trusted environment.

* When updating keys using the ECDH1 Deploy Mode, it provides higher security performance compared to the AES Deploy Mode. Since the value of k1 * G is independent of k2 and init_key, you can update the negotiated key in ECDH1 mode by updating only k2_info without changing k1*G. Users can:
  - Write k1 * G into the firmware in a trusted environment.
  - When updating the key using the ECDH1 Deploy Mode, transmit only init_key and k2_info. In this case, users can deploy the key in ECDH1 mode using sw_init_key even in an untrusted environment.

31.6.2.5 Private Key Recovery Mode

After deploying the private key, users can restore it using the key_info generated during deployment. The specific process is as follows.
1. Read the key_info from the external memory and store it to the fixed address in the internal memory of Key Manager.
2. Wait for the Key Manager to complete the deployment.
3. Repeat Step 1 ~ Step 2 above until all required private keys are restored.

Note that if two or more private keys with the same key_purpose are restored, only the last one will take effect. For more information about key_purpose, see Section 3.
```