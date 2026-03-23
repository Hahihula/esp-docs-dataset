

```markdown
Chapter 17 System Registers

GoBack

## 17.5 Registers

The addresses in this section are relative to System Registers base address provided in Table 5.3-2 in Chapter 5 System and Memory.

Register 17.1. HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG (0x0000)

| Bit 31 | ... | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 | Reset |
|--------|-----|-------|-------|-------|-------|-------|-------|
| O      | ... | reserved | HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT | HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT | HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT | (reserved) | 

HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT Configures whether or not to enable MSPI XTS manual encryption in SPI boot mode.  
O: Disable  
1: Enable  
(R/W)

HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT Configures whether or not to enable MSPI XTS auto decryption in download boot mode.  
O: Disable  
1: Enable  
(R/W)

HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT Configures whether or not to enable MSPI XTS manual encryption in download boot mode.  
O: Disable  
1: Enable  
(R/W)
```