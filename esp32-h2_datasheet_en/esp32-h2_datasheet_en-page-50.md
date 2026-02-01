**Title: Functional Description**

---

### **4.3 Wireless Communication**

This section describes the chip's wireless communication capabilities, spanning radio technology (Bluetooth Low Energy), and 802.15.4.

#### **4.3.1 Radio**

This subsection describes the fundamental radio technology embedded in the chip that facilitates wireless communication and data exchange.

##### **4.3.1.1 2.4 GHz Receiver**

The 2.4 GHz receiver demodulates the 2.4 GHz RF signal to baseband signals and converts them to the digital domain with two high-resolution ADCs. To adapt to varying signal channel conditions, ESP32-H2 integrates RF filters, Automatic Gain Control (AGC), DC offset cancellation circuits, and baseband filters.

##### **4.3.1.2 2.4 GHz Transmitter**

The 2.4 GHz transmitter modulates the baseband signals to the 2.4 GHz RF signal, and drives the antenna with a CMOS power amplifier.
Additional calibrations are integrated to cancel any radio imperfections, such as:
- Carrier leakage
- I/Q amplitude/phase matching

These built-in calibration routines reduce the cost, time, and specialized equipment required for product testing.

#### **4.3.2 Bluetooth LE**

ESP32-H2 includes a Bluetooth Low Energy subsystem that integrates a link controller, an RF/modem block and a feature-rich software protocol stack. It supports the core features of Bluetooth 5 and Bluetooth mesh.

##### **4.3.2.1 Bluetooth LE PHY**

ESP32-H2’s Bluetooth Low Energy PHY supports:
- 1 Mbps PHY
- 2 Mbps PHY for higher data rates

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback ESP32-H2 Series Datasheet v1.2