**Chapter 5 eFuse Controller (EFUSE)**

| Name | Bit width | Program | Software-Read Description |
|------|-----------|---------|-----------------------------|
| XPD_SDIO_REG | - | Protection by efuse_wr_disable | Protection by efuse_rd_disable |
| SDIO_TIEH | - | 5 | configures the flash regulator voltage: set to 1 for 3.3 V and set to 0 for 1.8 V |
| sdio_force | - | XPD_SDIO_REG and SDIO_TIEH can control the flash regulator | determines whether |
| BLK3_part_reserve | - | controls the eFuse controller | configures the SPI I/O to a certain pad |
| SPI_pad_config_clk | 5 | 6 | configures the SPI I/O to a certain pad |
| SPI_pad_config_q | 5 | 6 | configures the SPI I/O to a certain pad |
| SPI_pad_config_d | 5 | 6 | configures the SPI I/O to a certain pad |
| SPI_pad_config_cs0 | 5 | 6 | configures the SPI I/O to a certain pad |
| flash_crypt_config | - | governs flash encryption/decryption | controls the eFuse Controller |
| coding_scheme* | 2 | 10 | disables the ROM BASIC debug console fallback mode when set to 1 determines the status of Secure Boot |
| console_debugdisable | - | 15 | determines the status of Secure Boot |
| abstract_done_0 | - | 12 | determines the status of Secure Boot |
| abstract_done_1 | - | 13 | disables access to the JTAG controllers so as to effectively disable external use of JTAG |
| download_dis_encrypt | - | 15 | governs flash encryption/decryption |
| download_dis_decrypt | - | 15 | governs flash encryption/decryption |
| download_dis_cache | - | 15 | disables cache when boot mode is the Download Mode determines whether BLOCK3 is deployed for user purposes |
| key_status | - | 10 | governs flash encryption/decryption |

*Note: The asterisks (*) next to "coding_scheme" and "BLOCK1" indicate that these entries have special notes or conditions associated with them, which are not detailed in the provided text.