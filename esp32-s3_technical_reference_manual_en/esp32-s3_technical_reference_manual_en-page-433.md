**Chapter Title:**
Chapter 5 eFuse Controller

**Section Heading:**
Register 5.14. EFUSE_RD_REPEAT_DATA1_REG (0x034)

**Table Description:**
- The table lists various registers within the specified register, with their bit positions and descriptions.
- Bit positions are listed from right to left starting at '0'.
- Each row describes a specific bit or group of bits in terms of its function.

**Register Descriptions (Markdown format):**

1. **EFUSE_VDD_SPI_XPD**
   - Represents whether or not Flash Voltage Regulator is powered up.
   - 1: Powered up; 0: Not powered up
   - Access type: Read-only

2. **EFUSE_VDD_SPI_TIEH**
   - Represents whether or not Flash Voltage Regulator output is short connected to VDD3P3_RT_CIO_10.
   - 1: Short connected to VDD3P3_RTC_IO; 0: connect to 1.8V Flash Voltage Regulator
   - Access type: Read-only

3. **EFUSE_VDD_SPIFORCE**
   - Represents whether or not force using the parameters in eFuse, including EFUSE_VDD_SPI_XPD and EFUSE_VDD_SPI_TIEH, to configure flash voltage LDO.
   - 1: Use; 0: Not use
   - Access type: Read-only

4. **EFUSE_WDT_DELAY_SEL**
   - Represents RTC watchdog timeout threshold in slow clock cycle units (0x00).
   - Measurement unit:
     - 00: 4000, 
     - 01: 80000,
     - 10: 160000,
     - 11: 320000
   - Access type: Read-only

5. **EFUSE_SPI_BOOTCRYPT_CNT**
   - Represents whether SPI boot encrypt/decrypt is disabled or enabled.
   - Odd number of 1: Enabled; Even number including one bit set to 1: Disabled (RO)

6. **EFUSE_SECURE_BOOT_KEYREVOKE0, EFUSE_SECURE_BOOT_KEYREVOKE1, EFUSE_SECURE_BOOT_KEYREVOKE2**
   - Represents whether the first secure boot key is revoked.
   - 1: Revoked
   - Not revocation indicates no change in state.

7. **EFUSE_KEY_PURPOSE_0, EFUSE_KEY PURPOSE_1**
   - Represents purpose of Key0 and Key1 respectively (RO)

**Footer Information:**
- Page number: 433
- Document version: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Navigation Links:**
- Submit Documentation Feedback