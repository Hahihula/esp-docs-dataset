**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Body Text:**

- The RTC peripheral domain is powered down.
- The supply voltage to the RTC core drops to 0.7V.
- 8 x 32 bits of data are kept in general-purpose retention registers.
- The RTC memory and fast RTC memory are powered down.

- Current consumption: ~ 4.5 μA.

- Wake-up source: RTC timer only.

- Wake-up latency: less than 1 ms.

- Recommended for ultra-low-power infrequently-connected Wi-Fi/Bluetooth applications.

**Figure Description (with labels):**
Figure 9.3-9. Power Modes
- Sleep accept, Any interrupt, Modern sleep

**Diagram Labels and Flow:**
- Active mode → Digital&RTC pads, RTC timer, sdo, mic, uart, touch, co-processor, BT → Light sleep → Wake up time (arrow pointing upwards) → Deep sleep → Hibernate mode → Power consumption (arrow pointing downwards)

**Additional Text Below Diagrams:**

By default, ESP32 first enters the Modern-sleep mode after a system reset and can be configured to Active mode when transmitting or receiving packets. After the CPU stalls for a while, the chip can enter several low-power modes. It is up to the user to select the mode that best balances power consumption, wake-up latency and available wake-up sources. For details, please see Figure 9.3-9.

Please note that the predefined power mode could be further optimized and adapted to any application.

**Subsection Title:**
9.3.10 Wakeup Source

**Subsection Text:**

The ESP32 supports various wake-up sources, which could wake up the CPU in different sleep modes. The wake-up source is determined by RTC_CNTL_WAKEUP_ENA, as shown in Table 9.3-2.

**Footer Information:**
Espressif Systems
190
ESP32 TRM (Version 5.6)
Submit Documentation Feedback