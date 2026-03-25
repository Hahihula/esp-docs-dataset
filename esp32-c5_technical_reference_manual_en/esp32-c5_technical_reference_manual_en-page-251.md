

```markdown
| Parameters | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Description |
|:------------------------------------------------------------------|:-----------|:------------------------|:---------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EFUSE_DIS_PAD_JTAG | 1 | Y | 2 | Represents whether PAD JTAG is disabled in the hard way (permanently). |
| EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT | 1 | Y | 2 | Represents whether flash encryption is disabled (except in SPI boot mode). |
| EFUSE_USB_EXCHG_PINS | 1 | Y | 30 | Represents whether the D+ and D- pins is exchanged. |
| EFUSE_VDD_SPI_AS_GPIO | 1 | Y | 30 | Represents whether VDD SPI pin is functioned as GPIO. |
| EFUSE_WDT_DELAY_SEL | 2 | Y | 3 | Represents RTC watchdog timeout threshold. |
| EFUSE_BOOTLOADER_ANTI_ROLLBACK_SECURE_VERSION_LO | 3 | N | N/A | Represents the anti-rollback secure version of the second stage bootloader used by the first stage (ROM bootloader [the low part of the field]). |
| EFUSE_KM_DISABLE_DEPLOY_MODE | 4 | Y | 1 | Represents whether the new key deployment of key manager is disabled. |
| EFUSE_KM_RND_SWITCH_CYCLE | 2 | Y | 1 | Represents the cycle at which the Key Manager switches random numbers. |
| EFUSE_KM_DEPLOY_ONLY_ONCE | 4 | Y | 1 | Represents whether the corresponding key can be deployed only once. |
| EFUSE_FORCE_USE_KEY_MANAGER_KEY | 4 | Y | 1 | Represents whether the corresponding key must come from Key Manager. |
| EFUSE_FORCE_DISABLE_SW_INIT_KEY | 1 | Y | 1 | Represents whether to disable the use of the initialization key written by software and instead force use efuse_init_key. |
| EFUSE_BOOTLOADER_ANTI_ROLLBACK_UPDATE_IN_ROM | 1 | N | N/A | Represents whether the anti-rollback SECURE_VERSION will be updated from the ROM bootloader. |
| EFUSE_SPI_BOOT_CRYPT_CNT | 3 | Y | 4 | Represents whether SPI boot encryption/decryption is enabled. |
```