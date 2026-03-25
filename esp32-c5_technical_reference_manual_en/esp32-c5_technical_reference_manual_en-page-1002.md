
```markdown
Chapter 31 Key Manager

GoBack

2. Configure Static Parameters: Set the following parameters, including eFuse bits, registers and their corresponding locks:

* EFUSE_KM_INIT_KEY: 256-bit initial key used by the Key Manager in AES Deploy Mode and ECDH1 Deploy Mode.
* EFUSE_KM_DEPLOY_ONLY_ONCE: Controls whether the corresponding private key can only be deployed once after a power-on.

    - Bit[0]: Configures whether ECDSA key can be deployed only once.
        * 0: ECDSA key can be deployed more than once.
        * 1: ECDSA key can be deployed only once.

    - Bit[1]: Configures whether XTS key can be deployed only once.
        * 0: XTS key can be deployed more than once.
        * 1: XTS key can be deployed only once.

* EFUSE_FORCE_USE_KEY_MANAGER_KEY: Controls whether the corresponding private key must come from the Key Manager.

    - Bit[0]: Configures whether ECDSA key must come from the Key Manager.
        * 0: ECDSA key does not have to come from the Key Manager.
        * 1: ECDSA key must come from the Key Manager.

    - Bit[1]: Configures whether flash key must come from the Key Manager.
        * 0: Flash key does not have to come from the Key Manager.
        * 1: Flash key must come from the Key Manager.

    - Bit[2]: Configures whether HMAC key must come from the Key Manager.
        * 0: HMAC key does not have to come from the Key Manager.
        * 1: HMAC key must come from the Key Manager.

    - Bit[3]: Configures whether DSA key must come from the Key Manager.
        * 0: DSA key does not have to come from the Key Manager.
        * 1: DSA key must come from the Key Manager.

    - Bit[4]: Configures whether PSRAM key must come from the Key Manager.
        * 0: PSRAM key does not have to come from the Key Manager.
        * 1: PSRAM key must come from the Key Manager.

* KEYMNG_USE_EFUSE_KEY: Configures whether the key bit comes from eFuse block, valid only when the corresponding bit in EFUSE_FORCE_USE_KEY_MANAGER_KEY is 0.

    - Bit[0]: Configures whether ECDSA key comes from eFuse block.
        * 0: No effect.
        * 1: ECDSA key comes from eFuse block, valid only when bit[0] in EFUSE_FORCE_USE_KEY_MANAGER_KEY is 0.
```