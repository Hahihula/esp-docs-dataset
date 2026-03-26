

```markdown
Register 34.16. KEYMNG_STATIC_REG (0x0018)

KEYMNG_USE_EFUSE_KEY Configures whether or not to use eFuse key instead of Key Manager deployed key.

- Bit[0]: configures whether to use eFuse key for ECDSA key.
  0: No effect
  1: Use eFuse Key, valid only when bit[0] in EFUSE_FORCE_USE_KEY_MANAGER_KEY is 0.

- Bit[1] configures whether to use eFuse key for flash key.
  0: No effect
  1: Use eFuse Key, valid only when bit[1] in EFUSE_FORCE_USE_KEY_MANAGER_KEY is 0.

- Bit[2] configures whether to use eFuse key for HMAC key.
  0: No effect
  1: Use eFuse Key, valid only when bit[2] in EFUSE_FORCE_USE_KEY_MANAGER_KEY is 0.

- Bit[3] configures whether to use eFuse key for RSA_DS_KEY.
  0: No effect
  1: Use eFuse Key, valid only when bit[3] in EFUSE_FORCE_USE_KEY_MANAGER_KEY is 0.

- Bit[4] configures whether to use eFuse key for PSRAM key.
  0: No effect
  1: Use eFuse Key, valid only when bit[4] in EFUSE_FORCE_USE_KEY_MANAGER_KEY is 0.
(R/W)

KEYMNG_RND_SWITCH_CYCLE Configures cycles of the Key Manager to switch random numbers.

Measurement: Key Manager clock cycle.
This field is valid only when EFUSE_KM_RND_SWITCH_CYCLE is set to 0.

It is recommended to set this switch cycle to the number of Key Manager clock cycles corresponding to the TRNG module's clock cycle.
(R/W)

KEYMNG_USE_SW_INIT_KEY Configures whether or not to use sw_init_key, instead of EFUSE_KM_INIT_KEY, valid only when EFUSE_FORCE_DISABLE_SW_INIT_KEY is 0.

0: Use EFUSE_KM_INIT_KEY
1: Use software written sw_init_key
(R/W)
```
Continued on the next page...
```