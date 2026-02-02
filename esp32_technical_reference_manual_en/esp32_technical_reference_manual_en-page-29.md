**Chapter Title:**
Chapter 1

**Subheading and Content:**
ULP Coprocessor (ULP)

**Section Heading:** 
1.1 Introduction

**Body Text:**
The ULP coprocessor is an ultra-low-power processor that remains powered on during the Deep-sleep mode of the main SoC. Hence, the developer can store in the RTC memory a program for the ULP coprocessor to access peripheral devices, internal sensors and RTC registers during deep sleep. This is useful for designing applications where the CPU needs to be woken up by an external event, or timer, or a combination of these, while maintaining minimal power consumption.

**Section Heading:** 
1.2 Features

**List:**
- Contains up to 8 KB of SRAM for instructions and data
- Uses RTC_FAST_CLK, which is 8 MHz
- Works both in normal and deep sleep
- Is able to wake up the digital core or send an interrupt to the CPU
- Can access peripheral devices, internal sensors and RTC registers
- Contains four 16-bit general-purpose registers (R0, R1, R2, R3) for manipulating data and accessing memory
- Includes one 8-bit Stage_count register which can be manipulated by ALU and used in JUMP instructions

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)