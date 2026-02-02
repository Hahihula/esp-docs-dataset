**Chapter Title:**
Chapter 5

**Section Heading and Subsection Titles with Content:**

- **eFuse Controller (EFUSE)**
  - *Subsection 5.1 Introduction*
    - The ESP32 has a number of eFuses which store system parameters. Fundamentally, an eFuse is a single bit of non-volatile memory with the restriction that once an eFuse bit is programmed to 1, it can never be reverted to 0. Software can instruct the EFUSE Controller to program each bit for each system parameter as needed.
    - Some of these system parameters can be read by software using the eFuse Controller. Some of the system parameters are also directly used by hardware modules.

- **Subsection 5.2 Features**
  - Configuration of 33 system parameters
  - Optional write-protection
  - Optional software-read-protection

- **Subsection 5.3 Functional Description**

- **Subsection 5.3.1 Structure**
  - Thirty-three system parameters with different bit width are stored in the eFuses. The name of each system parameter and the corresponding bit width are shown in Table 5.3-1.
    - Among those parameters, efuse_wr_disable, efuse_rd_disable, BLK3_part_reserve and coding_scheme are directly used by the EFUSE Controller.

**Table Title:**
Table 5.3-1. System Parameters

| Name                | Bit width | Program                   | Software-Read Description |
|---------------------|-----------|---------------------------|----------------------------|
| efuse_wr_disable    | 16        | Protection by efuse_wr.disable | controls the EFUSE Controller |
| efuse_rd_disable    | 4         | -                        | controls the EFUSE Controller |
| flash_crypt_cnt     | 7         | -                        | governs the flash encryption/decryption |
| WIFI_MAC_Address    | 56        | Protection by Wi-Fi MAC address and CRC | -
| SPI_pad_config_hd  | 3         | -                        | configures the SPI I/O to a certain pad |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:**
GoBack