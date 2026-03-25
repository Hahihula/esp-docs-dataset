

# 19.5 Registers

In this section, addresses starting with HP_SYSTEM are relative to System Registers base address and addresses starting with LP_PERI are relative to LP Peripherals base address provided in Table 6.3-2 in Chapter 6 System and Memory.

## Register 19.1. HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG (0x0000)

```
31
+---------------------------------------------------------------+
| bit 31 | bit 30 | ... | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
|        |        |      |       |       |       |       | Reset |
+---------------------------------------------------------------+
```

**HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT** Configures whether to enable MSPI XTS manual encryption in SPI boot mode.

- 0: Disable
- 1: Enable
(R/W)

**HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT** Configures whether to enable MSPI XTS auto decryption in download boot mode.

- 0: Disable
- 1: Enable
(R/W)

**HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT** Configures whether to enable MSPI XTS manual encryption in download boot mode.

- 0: Disable
- 1: Enable
(R/W)