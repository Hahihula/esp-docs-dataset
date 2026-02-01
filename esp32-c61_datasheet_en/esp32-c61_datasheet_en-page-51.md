**Title: Functional Description**

---

### **4.3 Wireless Communication**

This section describes the chip's wireless communication capabilities, spanning radio technology, Wi-Fi, and Bluetooth.

#### **4.3.1 Radio**

This subsection describes the fundamental radio technology embedded in the chip that facilitates wireless communication and data exchange.

##### 4.3.1.1 2.4 GHz Receiver

The 2.4 GHz receiver demodulates the 2.4 GHz RF signal to quadrature baseband signals and converts them to the digital domain with two high-resolution, high-speed ADCs. To adapt to varying signal channel conditions, ESP32-C61 integrates RF filters, Automatic Gain Control (AGC), DC offset cancelation circuits, and baseband filters.

##### 4.3.1.2 2.4 GHz Transmitter

The 2.4 GHz transmitter modulates the quadrature baseband signals to the 2.4 GHz RF signal, and drives the antenna with a high-powered CMOS power amplifier. The use of digital calibration further improves the linearity of the power amplifier.

Additional calibrations are integrated to cancel any radio imperfections, such as:
- Carrier leakage
- I/Q amplitude/phase matching
- Baseband nonlinearities
- RF nonlinearities
- Antenna matching

These built-in calibration routines reduce the cost, time, and specialized equipment required for product testing.

#### **4.3.1.3 Clock Generator**

The clock generator produces quadrature clock signals of 2.4 GHz for both the receiver and the transmitter. All components of the clock generator are integrated into the chip, including inductors, varactors, filters, regulators, and dividers.

The clock generator has built-in calibration and self-test circuits. Quadrature clock phases and phase noise are optimized on-chip with patented calibration algorithms which ensure the best performance of the receiver and the transmitter.

#### **4.3.2 Wi-Fi**

This subsection describes the chip's Wi-Fi capabilities, which facilitate wireless communication at a high data rate.

---

**Footer:**
Espressif Systems
51 ESP32-C61 Series Datasheet v0.5