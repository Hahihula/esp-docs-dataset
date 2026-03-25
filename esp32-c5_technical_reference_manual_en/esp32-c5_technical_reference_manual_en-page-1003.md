

```markdown
- Bit[1]: Configures whether flash key comes from eFuse block.

  * 0: No effect.
  * 1: Flash key comes from eFuse block, valid only when bit[1] in `EFUSE_FORCE_USE_KEY_MANAGER_KEY` is 0.

- Bit[2]: Configures whether HMAC key comes from eFuse block.

  * 0: No effect.
  * 1: Flash key comes from eFuse block, valid only when bit[2] in `EFUSE_FORCE_USE_KEY_MANAGER_KEY` is 0.

- Bit[3]: Configures whether DSA key comes from eFuse block.

  * 0: No effect.
  * 1: DSA key comes from eFuse block, valid only when bit[1] in `EFUSE_FORCE_USE_KEY_MANAGER_KEY` is 0.

- Bit[4]: Configures whether PSRAM key comes from eFuse block.

  * 0: No effect.
  * 1: PSRAM key comes from eFuse block, valid only when bit[4] in `EFUSE_FORCE_USE_KEY_MANAGER_KEY` is 0.

• EFUSE_FORCE_DISABLE_SW_INIT_KEY: Controls whether the use of software-source `init_key` (`sw_init_key`) is permanently disabled.

  - 0: Not disabled.
  - 1: Permanently disabled.

• KEYMNG_USE_SW_INIT_KEY: Configures whether or not to use the software configured `sw_init_key` instead of a eFuse block with purpose of `EFUSE_KM_INIT_KEY`, valid only when `EFUSE_FORCE_DISABLE_SW_INIT_KEY` is 0.

  - 0: Use a eFuse block with purpose of `EFUSE_KM_INIT_KEY`.
  - 1: Use the software configured `sw_init_key`.

• EFUSE_KM_RND_SWITCH_CYCLE: Configures the interval for the Key Manager to switch random numbers. It is recommended to set this switch cycle to the number of Key Manager clock cycles corresponding to the TRNG module clock cycles.

  - 0: Switch cycle is controlled by `KEYMNG_RND_SWITCH_CYCLE`.
  - 1: 8 cycles of Key Manager clock.
  - 2: 16 cycles of Key Manager clock.
  - 3: 32 cycles of Key Manager clock.

• KEYMNG_RND_SWITCH_CYCLE: Configures the interval for the Key Manager to switch random numbers, valid only when `EFUSE_KM_RND_SWITCH_CYCLE` is 0. It is recommended to set this switch cycle to the number of Key Manager clock cycles corresponding to the TRNG module clock cycles.
```