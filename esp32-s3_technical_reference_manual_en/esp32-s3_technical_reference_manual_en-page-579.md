**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Table Header:**
Table 10.4-2. Predefined Power Modes

**Table Content:**

| **Power Mode** | PMU | RTC | Digital Peripherals System | CPU | PD | Wireless Circuits | RC_FAST_CLK | XTAL_CLK | PLL | RF Circuits |
|-----------------|-----|-----|----------------------------|-----|----|--------------------|-------------|----------|-----|------------|
| Active          | ON  | ON  | ON                         | ON  | ON | ON                  | ON          | ON       | ON   | ON         |
| Modem-sleep     | ON  | ON  | ON                         | ON  | ON | ON                  | ON          | ON       | ON   | OFF        |
| Light-sleep     | ON  | ON  | ON                         | ON  | ON | ON                  | OFF         | OFF      | OFF  | OFF        |
| Deep-sleep      | ON  | ON*| OFF                        | OFF | OFF| OFF                 | OFF         | OFF      | OFF  | OFF        |

**Note:**
*Configurable.*

**Body Text:**

By default, ESP32-S3 first enters the Modem-sleep mode after a system reset and can be configured to Active mode when transmitting or receiving packets. After the CPU stalls for a while, the chip can enter different low-power modes (including Modem-sleep, Light-sleep, and Deep-sleep) to save power. From Active to Deep-sleep, the number of available functionalities¹ and power consumption² decreases and wakeup latency increases. Also, the supported wakeup sources for different power modes are different³. Users can choose a power mode based on their requirements of performance, power consumption, wakeup latency, and available wakeup sources.

**Note:**
1. For details, please refer to Table 10.4-2.
2. For details on power consumption, please refer to the Current Consumption Characteristics in ESP32-S3 Datasheet.
3. For details on the supported wakeup sources, please refer to Section 10.4.4.

**Subsection Title:**
10.4.4 Wakeup Source

**Subsection Body Text:**

The ESP32-S3 supports various wakeup sources, which could wake up the CPU in different sleep modes. The wakeup source is determined by RTC_CNTL_RTC_WAKEUP_ENA as shown in Table 10.4-3.

**Footer Information:**
Espressif Systems
Page number: 579
Document version: ESP32-S3 TRM (Version 1.7)
Link to submit documentation feedback