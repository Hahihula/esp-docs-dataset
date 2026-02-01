Title: Functional Description

Subtitle: 4.3 Wireless Communication

Body Text:
This section describes the chip's wireless communication capabilities, spanning radio technology and Wi-Fi.

Subheading: 4.3.1 Radio

List:
- The ESP32-S2 radio consists of the following blocks:

    - 2.4 GHz receiver
    - 2.4 GHz transmitter
    - Bias and regulators
    - Balun and transmit-receive switch
    - Clock generator

Subheading: 4.3.1.1 2.4 GHz Receiver

Body Text:
The 2.4 GHz receiver demodulates the 2.4 GHz RF signal to quadrature baseband signals and converts them to the digital domain with two high-resolution, high-speed ADCs. To adapt to varying signal channel conditions, RF filters, Automatic Gain Control (AGC), DC offset cancelation circuits and baseband filters are integrated with ESP32-S2.

Subheading: 4.3.1.2 2.4 GHz Transmitter

Body Text:
The 2.4 GHz transmitter modulates the quadrature baseband signals to the 2.4 GHz RF signal, and drives the antenna with a high-powered Complementary Metal Oxide Semiconductor (CMOS) power amplifier. The use of digital calibration further improves the linearity of the power amplifier.

Additional calibrations are integrated to cancel any radio imperfections, such as:

- carrier leakage
- I/Q amplitude/phase matching
- baseband nonlinearities
- RF nonlinearities
- antenna matching

These built-in calibration routines reduce the cost, time, and specialized equipment required for product testing, and certification.

Subheading: 4.3.1.3 Clock Generator

Body Text:
The clock generator produces quadrature clock signals of 2.4 GHz for both the receiver and the transmitter. All components of the clock generator are integrated into the chip, including all inductors, varactors, filters, regulators and dividers.

The clock generator has built-in calibration and self-test circuits. Quadrature clock phases and phase noise are optimized on-chip with patented calibration algorithms which ensure the best performance of the receiver and the transmitter.

Footer:
Espressif Systems
46 ESP32-S2 Series Datasheet v1.8

Link: Submit Documentation Feedback