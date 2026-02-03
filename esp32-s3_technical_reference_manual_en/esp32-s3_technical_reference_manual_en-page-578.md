**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Table Title and Header:**
Table 10.4-1. RTC Statues Transition

| Category | Power Domain Sub-category | Active RTC Status |
|----------|---------------------------|--------------------|
|          |                          | Monitor Sleep      |

| RTC^1,2 | Power Management Unit^3   | ON                  | ON                 | ON                |
|         | RTC Peripherals^4         | ON                  | OFF                |                   |
|         | CPU^5                     | ON                  | OFF*               | OFF*             |
| Digital  | Wireless digital circuits^6 | ON              | OFF*               | OFF*             |
|         | Digital Core^7            | ON                  | OFF*               | OFF*             |
|         | PD Peripherals             | ON                  | OFF*               | OFF*             |
|         | RC_FAST_CLK^8             | ON                  | OFF                |                   |
| Analog   | XTAL_CLK^9                | ON                  | OFF                | OFF              |
|         | PLL                        | ON                  | OFF                | OFF              |
|         | RF Circuits                | -                   | -                  | -                |

**Body Text:**
Configurable.

1. RTC slow memory supports 8 KB SRAM, which can be used to reserve memory or to store ULP instructions and/or data. This memory (starting address is 0x5000_0000) can be accessed by CPU via PIF bus, and should be force-power-on. RTC slow memory is always OFF under the RTC state of Monitor with only one exception when the ULP coprocessor is working.
2. RTC fast memory supports 8 KB SRAM, which can be used to reserve memory. This memory can be accessed by CPU via IRAMO/DRAMO, and should be forced-power-up.

3. ESP32-S3's power management unit is specially designed to be "always-on", which means it is always on when the chip is powered up. Therefore, users cannot FPU or FPD the power management unit.
4. The RTC peripherals include 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V) and On-Chip Sensors and Analog Signal Processing^9 (i.e., temperature sensor controller and SAR ADC controller).
5. CPU can be powered down separately in light-sleep, but retention DMA is required to resume CPU.
6. Power domain Wireless digital circuits includes Wi-Fi MAC, BT and BB (Base Band).
7. When the digital core of the digital is powered down, all components in the digital are turned off. It's worth noting that, ESP32-S3’s ROM and SRAM are no longer controlled as independent power domains, thus cannot be force-powered-up or force-powered-down when the digital core is powered down.

**Subsection Title:**
10.4.3 Pre-defined Power Modes

**Body Text for Subsection:**
As mentioned earlier, ESP32-S3 has four power modes, which are predefined configurations that power up different combinations of power domains. For details, please refer to Table 10.4-2.

**Footer Information:**
Espressif Systems
578
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)