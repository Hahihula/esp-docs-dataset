**Title: Functional Description**

---

### **4.1.4.8 External Memory Encryption and Decryption**

The External Memory Encryption and Decryption (XTS_AES) module in the ESP32-H2 chip provides security for users’ application code and data stored in the external memory (flash).

#### Feature List
- General XTS-AES algorithm, compliant with IEEE Std 1619-2007
- Software-based manual encryption
- High-speed auto decryption without software’s participation
- Encryption and decryption functions jointly enabled/disabled by registers configuration, eFuse parameters, and boot mode
- Configurable Anti-DPA

- Pseudo-round anti-DPA function

For details, see [ESP32-H2 Technical Reference Manual > Chapter External Memory Encryption and Decryption (XTS_AES)](#).

---

### **4.1.4.9 Random Number Generator**

The Random Number Generator (RNG) in the ESP32-H2 is a true random number generator that generates 32-bit random numbers for cryptographic operations from a physical process.

#### Feature List
- RNG entropy source

  - Thermal noise from high-speed ADC or SAR ADC

  - An asynchronous clock mismatch

For more details about the Random Number Generator, refer to the [ESP32-H2 Technical Reference Manual > Chapter Random Number Generator (RNG)](#).

---

### **4.1.4.10 Power Glitch Detector**

The ESP32-H2 chip integrates a power glitch detector that monitors the voltage of power supply pins, including VDDPST1, VDDPST2, and VDD3P3 (PIN 27), in real time. It can detect voltage abnormalities occurring at these pins. For example, when a sudden voltage drop or voltage glitch is detected, the chip triggers a power glitch reset to ensure the system safely returns to a controllable state. This prevents logic errors, data loss, or hardware damage caused by power glitch.

#### Features
- Real-time monitoring of the voltage on specific power pins

- Ability to trigger a power glitch reset to prevent power glitch attacks

- Enabled by default at power-up

---

Espressif Systems  
38  
[Submit Documentation Feedback](#)  
ESP32-H2 Series Datasheet v1.2