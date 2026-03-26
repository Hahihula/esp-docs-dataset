

```markdown
Register 34.16. KEYMNG_STATIC_REG (0x0018)

Continued from the previous page...

KEYMNG_FLASH_KEY_LEN   Configures the key length for flash crypt.
    0: Use xts-aes-128
    1: Use xts-aes-256
    (R/W)

KEYMNG_PSRAM_KEY_LEN   Configures the key length for PSRAM crypt.
    0: Use xts-aes-128
    1: Use xts-aes-256
    (R/W)

Register 34.17. KEYMNG_LOCK_REG (0x001C)
```

```markdown
KEYMNG_USE_EFUSE_KEY_LOCK   Write 1 to lock KEYMNG_USE_EFUSE_KEY.
Each bit locks the corresponding bit of KEYMNG_USE_EFUSE_KEY.
(R/W1)

KEYMNG_RND_SWITCH_CYCLE_LOCK   Write 1 to lock KEYMNG_RND_SWITCH_CYCLE.
(R/W1)

KEYMNG_USE_SW_INIT_KEY_LOCK   Write 1 to lock KEYMNG_USE_SW_INIT_KEY.
(R/W1)

KEYMNG_FLASH_KEY_LEN_LOCK   Write 1 to lock KEYMNG_FLASH_KEY_LEN.
(R/W1)

KEYMNG_PSRAM_KEY_LEN_LOCK   Write 1 to lock KEYMNG_PSRAM_KEY_LEN.
(R/W1)
```

```plaintext
(reserved)                                 KEYMNG_PSRAM_KEY_LEN_LOCK
31    9 8 7 6 5 4 0
+----+----+----+----+----+----+----+
|    |    |    |    |    |    |Reset|
+----+----+----+----+----+----+----+
```