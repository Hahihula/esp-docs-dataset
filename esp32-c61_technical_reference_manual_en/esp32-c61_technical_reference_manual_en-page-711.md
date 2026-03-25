

# 17.5 Registers

In this section, addresses starting with HP_SYSTEM are relative to HP System Registers base address and addresses starting with LP_PERI are relative to Low-Power Peripherals base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 17.1. HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG (0x0000)

```
31
+---------------------------------------------------------------+
| bit 31 | bit 30 | ... | bit 8 | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
|        (reserved)                                Reset       |
+---------------------------------------------------------------+
```

HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT Configures whether to enable MSPI XTS manual encryption in SPI boot mode.
- O: Disable
- 1: Enable
(R/W)

HP_SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT Configures whether or not to enable Auto Encryption in Joint Download Boot mode.
- O: Disable
- 1: Enable
(R/W)

HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT Configures whether to enable MSPI XTS auto decryption in download boot mode.
- O: Disable
- 1: Enable
(R/W)

HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT Configures whether to enable MSPI XTS manual encryption in download boot mode.
- O: Disable
- 1: Enable
(R/W)