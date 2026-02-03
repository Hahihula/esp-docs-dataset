**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Titles and Content:**

### Introduction

ESP32-S3 has an advanced Power Management Unit (PMU), which can flexibly power up different power domains of the chip, to achieve the best balance among chip performance, power consumption, and wakeup latency. To simplify power management for typical scenarios, ESP32-S3 has predefined four power modes, which are preset configurations that power up different combinations of power domains. On top of that, the chip also allows the users to independently power up any particular power domain to meet more complex requirements. ESP32-S3 has integrated two Ultra-Low-Power coprocessors (ULP co-processors), which allow the chip to work when most of the power domains are powered down, thus achieving extremely low-power consumption.

### Features

ESP32-S3’s low-power management supports the following features:

- Four predefined power modes to simplify power management for typical scenarios
- Up to 16 KB of retention memory (slow memory and fast memory)
- 8 x 32-bit retention registers
- RTC Boot supported for reduced wakeup latency
- ULP co-processors supported in all power modes

In this chapter, we first introduced the working process of ESP32-S3’s low-power management, then introduce the predefined power modes of the chip, and at last, introduce the RTC boot of the chip.

### Functional Description

ESP32-S3's low-power management involves the following components:

- Power management unit: controls the power supply to three power domain categories
  - Real Time Controller (RTC)
  - Digital
  - Analog

For a complete list of 10 power domains grouped in these three power domain categories, see Section **10.4.1**.

---

**Footer Information:**
Espressif Systems  
565  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)