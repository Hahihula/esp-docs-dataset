

```markdown
Chapter 7 eFuse Controller (EFUSE)

Register 7.5. EFUSE_RD_REPEAT_DATA1_REG (0x0034)
```

Continued from the previous page...

```markdown
EFUSE_BOOTLOADER_ANTI_ROLLBACK_UPDATE_IN_ROM Represents whether the anti-rollback SECURE_VERSION will be updated from the ROM bootloader.

1: Enable
O: Disable
(RO)

EFUSE_SPI_BOOT_CRYPT_CNT Represents whether SPI boot encryption/decryption is enabled.
Odd count of bits with a value of 1: Enabled
Even count of bits with a value of 1: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKEO Represents whether revoking Secure Boot key digest 0 is enabled.
1: Enabled
O: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKE1 Represents whether revoking Secure Boot key digest 1 is enabled.
1: Enabled
O: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKE2 Represents whether revoking Secure Boot key digest 2 is enabled.
1: Enabled
O: Disabled
(RO)

EFUSE_KEY_PURPOSE_O Represents the purpose of Key0. See Table 7.3-2. (RO)

EFUSE_KEY_PURPOSE_1 Represents the purpose of Key1. See Table 7.3-2. (RO)
```