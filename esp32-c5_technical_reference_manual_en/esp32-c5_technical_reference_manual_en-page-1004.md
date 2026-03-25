

```markdown
3. Configure Working Mode: Configure `KEYMNG_KGEN_MODE` to complete the working mode configuration of the Key Manager as described in Section 31.6.2.

*   0: Random Deploy Mode
*   1: AES Deploy Mode
*   2: ECDHO Deploy Mode
*   3: ECDH1 Deploy Mode
*   4: Private Key Recovery mode
*   5: `key_info` Export Mode
*   Others: Not valid

4. Configure Target Key: Configure `KEYMNG_KEY_PURPOSE` to the target `key_purpose`:

*   1: `ecdsa_key`
*   2: `flash_256_key_1`
*   3: `flash_256_key_2`
*   4: `flash_128_key`
*   6: `hmac_key`
*   7: `dsa_key`
*   8: `psram_256_key_1`
*   9: `psram_256_key_2`
*   10: `psram_128_key`
*   Other values: Not valid

5. Transition to PREP Phase: Configure `KEYMNG_START` to complete the IDLE phase and enter the PREP phase.

### 31.7.2.2 PREP Phase

Users need to wait for the PREP phase to complete. This can be done using one of the following methods:

*   **Monitor `KEYMNG_STATE`:** Continuously check `KEYMNG_STATE` until it is no longer BUSY.
*   **Use Interrupt:** Enable the interrupt `KEYMNG_PREP_DONE_INT` and handle the completion in the interrupt service routine.

### 31.7.2.3 LOAD Phase

Users check `KEYMNG_STATE` to confirm that the Key Manager is in the LOAD phase. In the LOAD phase, users need to perform the following configurations.

1. Configure Based on Mode: Depending on the mode of the Key Manager, configure as follows:

    *   Random Deploy Mode: No additional configuration is required.
    *   AES Deploy Mode:
```