Title: Functional Description

Subtitle: Host Mode Features
- Bullet Point:
  - Eight channels (pipes)
    - Sub-bullet Points:
      - A control pipe consists of two channels (IN and OUT), as IN and OUT transactions must be handled separately. Only Control transfer type is supported.
      - Each of the other seven channels is dynamically configurable to be IN or OUT, and supports Bulk, Isochronous, and Interrupt transfer types.

- Bullet Point:
  - All channels share an RX FIFO, non-periodic TX FIFO, and periodic TX FIFO. The size of each FIFO is configurable.

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter USB On-The-Go.

Subtitle: Pin Assignment
For details, see Section **2.3.5 Peripheral Pin Assignment**.

Subtitle: 4.2.1.8 USB Serial/JTAG Controller

Body Text:
ESP32-S3 integrates a USB Serial/JTAG controller.
Feature List:

- Bullet Point:
  - USB Full-speed device.

- Bullet Point:
  - Can be configured to either use internal USB PHY of ESP32-S3 or external PHY via GPIO matrix.

- Bullet Point:
  - Fixed function device, hardwired for CDC-ACM (Communication Device Class - Abstract Control Model) and JTAG adapter functionality.
  
- Bullet Point:
  - Two OUT Endpoints, three IN Endpoints in addition to Control Endpoint; Up to 64-byte data payload size.

- Bullet Point:
  - Internal PHY, so no or very few external components needed to connect to a host computer.

- Bullet Point:
  - CDC-ACM adherent serial port emulation is plug-and-play on most modern OSes.
  
- Bullet Point:
  - JTAG interface allows fast communication with CPU debug core using a compact representation of JTAG instructions.

- Bullet Point:
  - CDC-ACM supports host controllable chip reset and entry into download mode.

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter USB Serial/JTAG Controller.

Subtitle: Pin Assignment
For details, see Section **2.3.5 Peripheral Pin Assignment**.

Subtitle: 4.2.1.9 SD/MMC Host Controller

Body Text:
ESP32-S3 has an SD/MMC Host controller.
Footer Information:

- Company Name: Espressif Systems
- Page Number and Document Version: 56 ESP32-S3 Series Datasheet v2.1
- Link: [Submit Documentation Feedback](#)