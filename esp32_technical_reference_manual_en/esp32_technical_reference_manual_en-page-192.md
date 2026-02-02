**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Body Text:**

by the CPU, thus guaranteeing the proper functioning of the peripherals.

Among the wakeup sources listed in Table 9.3-2, GPIO and SDIO can be configured as the causes to reject sleep.
Users can configure the reject to sleep option via the following registers:
- Configure the RTC_CNTL_SLP_REJECT field to enable or disable the option to reject to sleep:
  - Set RTC_CNTL_LIGHT_SLP_REJECT_EN to enable reject-to-light-sleep.
  - Set RTC_CNTL_DEEP_SLP_REJECT_EN to enable reject-to-deep-sleep.
- Read RTC_CNTL_REJECTCAUSE to check the reason for rejecting to sleep.

**Subsection Title:**
9.3.12 RTC Timer

**Subsection Body Text:**

The RTC timer is a 48-bit counter that can be read. The clock is RTC_SLOW_CLK. Any reset/sleep mode, except for the power-up reset, will not stop or reset the RTC timer.

The RTC timer can be used to wake up the CPU at a designated time, and to wake up TOUCH or the ULP coprocessor periodically.

**Subsection Title:**
9.3.13 RTC Boot

**Subsection Body Text:**

Since the CPU, ROM and RAM are powered down during Deep-sleep and Hibernate mode, the wake-up time is much longer than that in Light sleep/Modem sleep, because of the ROM unpacking and data-copying from the flash (SPI booting). There are two types of SRAM in the RTC, named slow RTC memory and fast RTC memory, which remain powered-on in Deep-sleep mode. For small-scale codes (less than 8 KB), there are two methods of speeding up the wake-up time, i.e., avoiding ROM unpacking and SPI booting.

The first method is to use the RTC slow memory:
1. Set register RTC_CNTL_PROCPU_STAT_VECTOR_SEL for PRO_CPU (or register RTC_CNTL_APPCPU_STAT_VECTOR_SEL for APP-CPU) to 0.
2. Put the chip into sleep.
3. When the CPU is powered up, the reset vector starts from 0x50000000, instead of 0x40000400. ROM unpacking & SPI boot are not needed. The code in RTC memory has to do itself some initialization for the C program environment.

The second method is to use the fast RTC memory:
1. Set register RTC_CNTL_PROCPU_STAT_VECTOR_SEL for PRO_CPU (or register RTC_CNTL_APPCPU_STAT_VECTOR_SEL for APP-CPU) to 1.
2. Calculate CRC for the fast RTC memory, and save the result in register RTC_CNTL_RTC_STORE6_REG[31:0].
3. Input register RTC_CNTL_RTC_STORE7_REG[31:0] with the entry addresss in the fast RTC memory.
4. Put the chip into sleep.
5. When the CPU is powered up, after ROM unpacking and some necessary initialization, the CRC is calculated again. If the result matches with register RTC_CNTL_RTC STORE6_REG[31:0], the CPU will jump to the entry address.

**Footer Text:**
Espressif Systems
Page number 192 (ESP32 TRM - Version 5.6)