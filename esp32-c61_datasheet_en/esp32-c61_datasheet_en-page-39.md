**Title: Functional Description**

---

### **4.1.3.8 Brownout Detector**

ESP32-C61 can periodically monitor the voltage of the power supply, and in the event of abnormal voltage, it is capable of generating interrupts or initiating resets.

- Feature List:
  - Configurable detection threshold
  - Configurable reset level
  - Glitch filtering

---

### **4.1.3.9 RTC Timer**

ESP32-C61 RTC Timer starts counting once the chip is powered on and keeps counting in any state.

- Feature List:
  - 46-bit counter operating under the RTC clock
  - Real-time reading of the time-base counter’s value
  - Configurable target value for the counter to trigger an interrupt upon timeout

---

### **4.1.3.10 Timer Group**

The Timer Group (TIMG) in the ESP32-C61 chip can be used to precisely time an interval, trigger an interrupt after a particular interval (periodically and aperiodically), or act as a hardware clock. ESP32-C61 has two timer groups, each consisting of one general-purpose timer and one Main System Watchdog Timer.

- Feature List:
  - 16-bit prescaler
  - 54-bit auto-reload-capable up-down counter
  - Able to read real-time value of the time-base counter
  - Halt, resume, and disable the time-base counter
  - Programmable alarm generation
  - Timer value reload (auto-reload at an alarm or a software-controlled instant reload)
  - RTC slow clock frequency calculation
  - Level interrupt generation
  - Real-time alarm events
  - Support for several ETM tasks and events

---

**Footer:**
Espressif Systems  
39 ESP32-C61 Series Datasheet v0.5