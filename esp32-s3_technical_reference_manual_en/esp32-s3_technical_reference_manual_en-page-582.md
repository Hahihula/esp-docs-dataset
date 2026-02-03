**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Title:**
10.6 RTC Boot

**Body Text:**

The wakeup time from Deep-sleep mode is much longer, compared to Light-sleep and Modem-sleep modes, because the ROMs and RAMs are both powered down in this case, and the CPU needs more time for SPI booting (data-copying from the flash). However, it’s worth noting that both RTC fast memory and RTC slow memory remain powered up in the Deep-sleep mode. Therefore, users can store codes (so called “deep sleep wake stub” of up to 8 KB) either in RTC fast memory or RTC slow memory, which doesn’t require the above-mentioned SPI booting, thus speeding up the wakeup process.

**Subsection Title:**
Method one: Boot using RTC slow memory

1. Set `RTC_CNTL_PROCPU_STAT_VECTOR_SEL` to 0.
2. Send the chip into sleep.
3. After the CPU is powered up, the reset vector starts resetting from Ox5000000 instead of 0x40000000, which does not involve any SPI booting. The codes stored in RTC slow memory starts running immediately after the CPU reset. The code stored in the RTC slow memory only needs to be partially initialized in a C environment.

**Subsection Title:**
Method two: Boot using RTC fast memory

1. Set `RTC_CNTL_PROCPU_STAT_VECTOR_SEL` to 1.
2. Calculate CRC for the RTC fast memory, and save the result in `RTC_CNTL_RTC_STORE7_REG[31:0]`.
3. Set `RTC_CNTL_RTC_STORE6_REG[31:0]` to the entry address of RTC fast memory.
4. Send the chip into sleep.

5. ROM unpacking and some of the initialization starts after the CPU is powered up. After that, the CRC for the RTC fast memory will be calculated again. If the result matches with register `RTC_CNTL_RTC_STORE7_REG[31:0]`, the CPU jumps to the entry address.

**Footer Text:**
The boot flow is shown in Figure 10.6-1

**Page Footer Information:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)