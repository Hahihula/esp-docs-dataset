**Chapter 5 eFuse Controller**

---

**GoBack**

Among these blocks, BLOCK4 ~ 9 store KEY0 ~ 5, respectively. Up to six 256-bit keys can be written into eFuse. Whenever a key is written, its purpose value should also be written (see table *5.3-2*). For example, when a key for the JTAG function in HMAC Downstream mode is written to KEY3 (i.e., BLOCK7), its key purpose value 6 should also be written to EFUSE_KEY_PURPOSE_3.

BLOCK1 ~ BLOCK10 use the RS coding scheme, so there are some restrictions on writing to these parameters. For more detailed information, please refer to Section *5.3.1.3* and *5.3.2*.

---

**5.3.1.1 EFUSE_WR_DIS**

Parameter **EFUSE_WR_DIS** determines whether individual eFuse parameters are write-protected. After **EFUSE_WR_DIS** has been programmed, execute an eFuse read operation to let the new values take effect (see Section *5.3.3*).

Column “Write Protection by **EFUSE_WR_DIS** Bit Number” in Table 5.3-1 and Table 5.3-3 list the specific bits in EFUSE_WR_DIS that disable writing.

When the write protection bit of a parameter is set to 0, it means that this parameter is not write-protected and can be programmed.

Setting the write protection bit of a parameter to 1 enables write-protection for it and none of its bits can be modified afterwards. Non-programmed bits always remain 0 while programmed bits always remain 1.

---

**5.3.1.2 EFUSE_RD_DIS**

Only the eFuse blocks BLOCK4 ~ BLOCK10 can be individually read protected to prevent any access from outside the chip, as shown in column “Read Protection by **EFUSE_RD_DIS** Bit Number” of Table *5.3-3*. After **EFUSE_RD_DIS** has been programmed, execute an eFuse read operation to let the new values take effect (see Section *5.3.3*).

If a bit in **EFUSE_RD_DIS** is 0, then the eFuse block can be read by users; if a bit in **EFUSE_RD_DIS** is 1, then the parameter controlled by this bit is user read protected.

Other parameters that are not in BLOCK4 ~ BLOCK10 can always be read by users.

When BLOCK4 ~ BLOCK10 are set to be read-protected, the data in these blocks are not readable by users, but they can still be used internally by hardware cryptography modules, if the EFUSE_KEY PURPOSE_n bit is set accordingly.

---

**5.3.1.3 Data Storage**

According to the different types of eFuse bits, eFuse controller use two hardware encoding schemes to protect eFuse bits from corruption.

All BLOCK0 parameters except for **EFUSE_WR_DIS** are stored with four backups, meaning each bit is stored four times. This scheme is transparent to the user. This encoding scheme is invisible for users.

BLOCK1 ~ BLOCK10 store key data and some parameters and use RS (44, 32) coding scheme that supports up to 6 bytes of automatic error correction. The primitive polynomial of RS (44, 32) is

p(x) = x^8 + x^4 + x^3 + x^2 + 1.

The shift register circuit shown in Figure *5.3-1* and *5.3-2* processes 32 bytes data using RS (44, 32). This coding scheme encodes 32 bytes of data into 44 bytes:

---

**Espressif Systems**

**417 ESP32-S3 TRM (Version 1.7)**

**Submit Documentation Feedback**