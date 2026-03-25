

```markdown
Register 7.8. EFUSE_RD_REPEAT_DATA4_REG (0x0040)

EFUSE_HUK_GEN_STATE Represents whether the HUK generate mode is valid.
Odd count of bits with a value of 1: Invalid
Even count of bits with a value of 1: Valid
(RO)

EFUSE_ECC_FORCE_CONST_TIME Represents whether to force ECC to use constant-time mode for point multiplication calculation.
0: Not force
1: Force
(RO)

EFUSE_RECOVERY_BOOTLOADER_FLASH_SECTOR_LO Represents the starting flash sector (flash sector size is 0x1000) of the recovery bootloader used by the ROM bootloader. If the primary bootloader fails, 0 and 0xFF - this feature is disabled. (The low part of the field). (RO)

Register 7.9. EFUSE_RD_MAC_SYSO_REG (0x0044)

EFUSE_MAC_O Represents the lower 32 bits of MAC address. (RO)
```