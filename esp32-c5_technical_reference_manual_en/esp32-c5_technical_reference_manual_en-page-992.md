

```markdown
Chapter 31 Key Manager

GoBack

31.6.1.2 HUK Status Check

Users can read the register HUK_STATUS_REG to check the current status of the HUK and decide whether to regenerate the HUK. HUK_STATUS_REG has the following fields:

- **HUK_STATUS**: Indicates the current status of the HUK.
  - 0: The HUK has not been generated
  - 1: The HUK has been successfully generated and is valid
  - 2: The HUK has been generated but is invalid
  - 3: Reserved

- **HUK_RISK_LEVEL**: Indicates the current risk level of the HUK. The value ranges from 0 to 7, with higher values indicating greater risk. When the value is 7, the HUK is no longer available. At this point, the HUK_STATUS will be set to 2.

Note:

- HUK Generator uses the default value of SRAM PUF to generate HUK. The HUK risk level refers to the difference between the current default value of SRAM PUF and the default value of SRAM PUF at the time when the HUK was created.
- In certain special applications, such as when users want to discard a key and invalidate the corresponding key_info, they can select to update the HUK. Once the HUK is changed, the previously deployed key, as well as its key_info, both become invalid, i.e., the new huk_info together with the previous key_info can not be used to recover the key.

31.6.2 Key Manager

Note:
Each time before using the Key Manager for key deployment, please ensure that the HUK is valid by checking the register HUK_STATUS_REG.

Key Manager provides the following modes:

- **Key Deployment Modes:**
  - Random Deploy Mode: Deploys a random private key.
  - AES Deploy Mode: Deploys a specified private key.
  - ECDHO Deploy Mode: Deploys a negotiated private key.
  - ECDH1 Deploy Mode: Deploys a negotiated private key.

These four deployment modes allow users to select the most convenient deployment process in environments with different security levels according to their own needs.

- **Key Recovery Mode:**
  - Private Key Recovery Mode: Recovers the deployed private key.

This recovery mode allows users to freely select the key they want to recover from any number of the deployed keys.
```