

```markdown
Register 34.18. KEYMNG_CONF_REG (0x0020)

KEYMNG_KGEN_MODE Configures deployment mode.
0: Random Deploy Mode
1: AES Deploy Mode
2: ECDH0 Deploy Mode
3: ECDH1 Deploy Mode
4: Private Key Recovery Mode
5: key_info Export Mode
6~7: Reserved
(R/W)

KEYMNG_KEY_PURPOSE Configures key purpose.
1: ecdsa_key_192
2: ecdsa_key_256
3: flash_256_1_key
4: flash_256_2_key
5: flash_128_key
6: hmac_key
7: ds_key
8: psram_256_1_key
9: psram_256_2_key
10: psram_128_key
11: ecdsa_key_384_l
12: ecdsa_key_384_h
Others: Reserved
(R/W)
```