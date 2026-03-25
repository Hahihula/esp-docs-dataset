

# Chapter 16 System Registers

## GoBack

### 16.4 Registers

The addresses related to LP Peripheral timeout registers are relative to Low-power Peripheral base address provided in Table 4.3-2 in Chapter 4 System and Memory, and the others addresses in this section are relative to System Registers base address provided in Table 4.3-2 in Chapter 4 System and Memory.

#### Register 16.1. HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG (0x0000)

```
31
+---------------------------------------------------------------+
| HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT | HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT | HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT |
| (reserved)                                 | (reserved)                                | (reserved)                               |
+---------------------------------------------------------------+
Reset
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