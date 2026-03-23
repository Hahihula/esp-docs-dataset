

```markdown
| Parameters                                 | Bit Width | Accessible by Hardware | Programming-Protection by EFUSE_WR_DIS Bit Number | Description                                                                 |
|--------------------------------------------|-----------|------------------------|--------------------------------------------------|-----------------------------------------------------------------------------|
| EFUSE_WR_DIS                               | 32        | Y                      | N/A                                              | Represents whether writing of individual eFuses is disabled.                |
| EFUSE_RD_DIS                               | 7         | Y                      | 0                                                | Represents whether users’ reading from BLOCK4 ~ 10 is disabled.             |
| EFUSE_DIS_ICACHE                           | 1         | Y                      | 2                                                | Represents whether iCache is disabled.                                     |
| EFUSE_DIS_USB_JTAG                         | 1         | Y                      | 2                                                | Represents whether the USB-to-JTAG function is disabled.                    |
| EFUSE_DIS_DOWNLOAD_ICACHE                  | 1         | Y                      | 2                                                | Represents whether iCache is disabled in Download mode.                     |
| EFUSE_DIS_USB_SERIAL_JTAG                  | 1         | Y                      | 2                                                | Represents whether the usb_serial_jtag peripheral is disabled.              |
| EFUSE_DIS_FORCE_DOWNLOAD                   | 1         | Y                      | 2                                                | Represents whether the function to force the chip into Download mode is disabled. |
| EFUSE_DIS_TWAI                             | 1         | Y                      | 2                                                | Represents whether the TWAI controller is disabled.                         |
| EFUSE_JTAG_SEL_ENABLE                      | 1         | Y                      | 2                                                | Represents whether to use JTAG directly.                                   |
| EFUSE_SOFT_DIS_JTAG                        | 3         | Y                      | 31                                               | Represents whether JTAG is disabled in the soft way.                        |
| EFUSE_DIS_PAD_JTAG                         | 1         | Y                      | 2                                                | Represents whether JTAG is disabled in the hard way (permanently).           |
| EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT          | 1         | Y                      | 2                                                | Represents whether flash encryption is disabled in Download boot mode.       |
| EFUSE_USB_EXCHG_PINS                       | 1         | Y                      | 30                                               | Represents whether the D+ and D- pins are exchanged.                        |
| EFUSE_VDD_SPI_AS_GPIO                      | 1         | N                      | 30                                               | Represents whether the VDD_SPI pin is used as a regular GPIO.               |
| EFUSE_WDT_DELAY_SEL                        | 2         | Y                      | 3                                                | Represents whether RTC watchdog timeout threshold is selected.               |
| EFUSE_SPI_BOOT_CRYPT_CNT                   | 3         | Y                      | 4                                                | Represents whether SPI boot encryption/decryption is enabled.                |
```