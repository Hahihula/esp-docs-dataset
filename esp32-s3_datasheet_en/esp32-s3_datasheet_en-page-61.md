Title: Functional Description

Subtitle: 4.3 Wireless Communication

Body Text:
This section describes the chip's wireless communication capabilities, spanning radio technology, Wi-Fi, Bluetooth, and 802.15.4.

Subheading: 4.3.1 Radio

Body Text:
This subsection describes the fundamental radio technology embedded in the chip that facilitates wireless communication and data exchange.

Sub-subheading: 4.3.1.1 2.4 GHz Receiver

Body Text:
The 2.4 GHz receiver demodulates the 2.4 GHz RF signal to quadrature baseband signals and converts them to the digital domain with two high-resolution, high-speed ADCs. To adapt to varying signal channel conditions, ESP32-S3 integrates RF filters, Automatic Gain Control (AGC), DC offset cancelation circuits, and baseband filters.

Sub-subheading: 4.3.1.2 2.4 GHz Transmitter

Body Text:
The 2.4 GHz transmitter modulates the quadrature baseband signals to the 2.4 GHz RF signal, and drives the antenna with a high-powered CMOS power amplifier. The use of digital calibration further improves the linearity of the power amplifier.

To compensate for receiver imperfections, additional calibration methods are built into the chip,
including:
- Carrier leakage compensation
- I/Q amplitude/phase matching
- Baseband nonlinearities suppression
- RF nonlinearities suppression
- Antenna matching

These built-in calibration routines reduce the cost and time to the market for your product, and eliminate the need for specialized testing equipment.

Subheading: 4.3.1.3 Clock Generator

Body Text:
The clock generator produces quadrature clock signals of 2.4 GHz for both the receiver and the transmitter. All components of the clock generator are integrated into the chip, including inductors, varactors, filters, regulators, and dividers.

The clock generator has built-in calibration and self-test circuits. Quadrature clock phases and phase noise are optimized on chip with patented calibration algorithms which ensure the best performance of the receiver and the transmitter.

Subheading: 4.3.2 Wi-Fi

Body Text:
This subsection describes the chip's Wi-Fi capabilities, which facilitate wireless communication at a high data rate.

Footer Information (centered):
Espressif Systems
61
Submit Documentation Feedback ESP32-S3 Series Datasheet v2.1