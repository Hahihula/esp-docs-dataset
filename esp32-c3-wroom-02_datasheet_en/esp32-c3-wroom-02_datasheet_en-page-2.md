**1 Module Overview**

Note:
Check the link or the QR code to make sure that you use the latest version of this document:  
[https://www.espressif.com/documentation/esp32-c3-wroom-02_datasheet_en.pdf](https://www.espressif.com/documentation/esp32-c3-wroom-02_datasheet_en.pdf)

**1.1 Features**

* **CPU and On-Chip Memory**
  - ESP32-C3 embedded, 32-bit RISC-V single-core processor, up to 160 MHz
  - 384 KB ROM
  - 400 KB SRAM (16 KB for cache)
  - 8 KB SRAM in RTC

* **Wi-Fi**
  - IEEE 802.11b/g/n-compliant
  - Center frequency range of operating channel: 2412 ~ 2484 MHz
  - Supports 20 MHz, 40 MHz bandwidth in 2.4 GHz band
  - 1T1R mode with data rate up to 150 Mbps
  - Wi-Fi Multimedia (WMM)
  - TX/RX A-MPDU, TX/RX A-MSDU
  - Immediate Block ACK
  - Fragmentation and defragmentation
  - Transmit opportunity (TXOP)
  - Automatic Beacon monitoring (hardware TSF)
  - 4 × virtual Wi-Fi interfaces
  - Simultaneous support for Infrastructure BSS in Station mode, SoftAP mode, Station + SoftAP mode, and promiscuous mode

* **Bluetooth®**
  - Bluetooth LE: Bluetooth 5, Bluetooth mesh
  - Speed: 125 Kbps, 500 Kbps, 1 Mbps, 2 Mbps
  - Advertising extensions
  - Multiple advertisement sets
  - Channel selection algorithm #2
  - Internal co-existence mechanism between Wi-Fi and Bluetooth to share the same antenna

* **Peripherals**
  - Up to 15 GPIOs
    - 3 strapping GPIOs
  - SPI, UART, I2C, 2S, remote control peripheral, LED PWM controller, general DMA controller, TWAI® controller (compatible with ISO 11898-1, MSDU)
  - USB Serial/JTAG controller, temperature sensor, SAR ADC, general-purpose timers, watchdog timers

* **Integrated Components on Module**
  - 40 MHz crystal oscillator
  - SPI flash
  
**Antenna Options**
- ESP32-C3-WROOM-02: On-board PCB antenna  
- [ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6](#)

Espressif Systems

Submit Documentation Feedback