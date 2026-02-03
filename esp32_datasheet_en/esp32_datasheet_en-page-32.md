Title: Functional Description

Body Text:
interrupt, CPU reset, core reset, and system reset. Only the RWDT can trigger the system reset, and is able to reset the entire chip, including the RTC itself. A timeout value can be set for each stage individually.

During flash boot the RWDT and the first MWDT start automatically in order to detect, and recover from, booting problems.

The watchdogs have the following features:

- Four stages, each of which can be configured or disabled separately
- A programmable time period for each stage
- One of three or four possible actions (interrupt, CPU reset, core reset, and system reset) upon the expiry of each stage
- 32-bit expiry counter
- Write protection that prevents the RWDT and MWDT configuration from being inadvertently altered
- SPI flash boot protection

If the boot process from an SPI flash does not complete within a predetermined time period, the watchdog will reboot the entire system.

For details, see [ESP32 Technical Reference Manual](#) > Chapter Watchdog Timers.

Subtitle: 4.5 Cryptographic Hardware Accelerators

Body Text:
ESP32 is equipped with hardware accelerators of general algorithms, such as AES (FIPS PUB 197), SHA (FIPS PUB 180-4), and RSA. The chip also supports independent arithmetic, such as large-number modular multiplication and large-number multiplication. The maximum operation length for RSA, large-number modular multiplication, and large-number multiplication is 4096 bits.

The hardware accelerators greatly improve operation speed and reduce software complexity. They also support code encryption and dynamic decryption, which ensures that code in the flash will not be hacked.

Subtitle: 4.6 Radio and Wi-Fi

Body Text:
The radio module consists of the following blocks:

- **2.4 GHz receiver**
- **2.4 GHz transmitter**
- Bias and regulators
- Balun and transmit-receive switch
- Clock generator

Subtitle: 4.6.1 2.4 GHz Receiver

Body Text:
The 2.4 GHz receiver demodulates the 2.4 GHz RF signal to quadrature baseband signals and converts them to the digital domain with two high-resolution, high-speed ADCs. To adapt to varying signal channel conditions, RF filters, Automatic Gain Control (AGC), DC offset cancelation circuits and baseband filters are integrated in the chip.

Footer:
Espressif Systems
32 ESP32 Series Datasheet v5.2

Link: [Submit Documentation Feedback](#)