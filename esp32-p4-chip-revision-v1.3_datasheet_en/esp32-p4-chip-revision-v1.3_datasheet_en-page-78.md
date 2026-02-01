**Title: Functional Description**

---

### Pin Assignment

The temperature sensor does not directly interact with IOs, so it has no pins assigned.

#### **4.2.3.3 ADC Controller (ADC)**

ESP32-P4 integrates two 12-bit successive approximation ADCs (SAR ADCs) for measuring analog signals from up to 14 pins.

**Feature List**
- HP ADC and LP ADC controllers can control the SAR ADC via software
- 12-bit resolution
- Analog input sampling from up to 14 pins

**HP ADC controllers:**
- Multi-channel sampling control module with configurable channel sampling sequence
- Mode control module supporting dual HP ADC sampling
- Two filters with configurable filter coefficients
- Two threshold monitors that trigger an interrupt when filtered data exceeds a high threshold or falls below a low threshold
- Continuous transfer of conversion results to memory via the GDMA interface

**LP ADC controllers:**
- One-shot sampling mode
- Sampling in sleep mode (e.g., Deep-sleep)
- Event Task Matrix (ETM) support for various events and tasks

---

### Pin Assignment

The pins of the ADC controller are multiplexed with GPIO16 - GPIO23, GPIO49 - GPIO54; the interfaces of two analog voltage comparators. and the third RMMI interface of EMAC.

#### **4.2.3.4 Analog Voltage Comparator**

ESP32-P4 integrates two analog voltage comparators. These comparators rely on special pads that support voltage comparison functionality to monitor voltage changes on these pads.

**Feature List**
- Voltage comparison
  - Configurable voltage comparison mode
  - Configurable reference voltage
- Interrupt upon changes of voltage comparison result

---

Espressif Systems  
78  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)