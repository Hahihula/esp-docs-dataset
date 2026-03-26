

```markdown
Chapter 34 Key Manager

- 1: 8 cycles of Key Manager clock.
- 2: 16 cycles of Key Manager clock.
- 3: 32 cycles of Key Manager clock.

* KEYMNG_RND_SWITCH_CYCLE: Configures the interval for the Key Manager to switch random numbers, valid only when EFUSE_KM_RND_SWITCH_CYCLE is 0. It is recommended to set this switch cycle to the number of Key Manager clock cycles corresponding to the TRNG module clock cycles.

4. Configure Working Mode: Configure KEYMNG_KGEN_MODE to complete the working mode configuration of the Key Manager as described in Section 34.6.2.
    * 0: Random Deploy Mode
    * 1: AES Deploy Mode
    * 2: ECDHO Deploy Mode
    * 3: ECDH1 Deploy Mode
    * 4: Private Key Recovery mode
    * 5: key_info Export Mode
    * Others: Not valid

5. Configure Target Key: Configure KEYMNG_KEY_PURPOSE to the target key_purpose:
    * 1: ecdsa_key_192
    * 2: ecdsa_key_256
    * 3: flash_256_1_key
    * 4: flash_256_2_key
    * 5: flash_128_key
    * 6: hmac_key
    * 7: ds_key
    * 8: psram_256_1_key
    * 9: psram_256_2_key
    * 10: psram_128_key
    * 11: ecdsa_key_384_l
    * 12: ecdsa_key_384_h
    * Other values: Not valid

6. Transition to PREP Phase: Configure KEYMNG_START to complete the IDLE phase and enter the PREP phase.
```