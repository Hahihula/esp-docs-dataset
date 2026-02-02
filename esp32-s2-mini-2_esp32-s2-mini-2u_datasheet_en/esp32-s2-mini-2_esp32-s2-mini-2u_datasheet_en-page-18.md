**Title: Electrical Characteristics**

---

### Subtitle

- **5.4 Current Consumption Characteristics**
  
  Owing to the use of advanced power-management technologies, the module can switch between different power modes. For details on different power modes, please refer to Section RTC and Low-Power Management in ESP32-S2 Series Datasheet.

#### Subsection: 
**5.4.1 Current Consumption in Active Mode**

- **Table 5-4. RF Current Consumption in Active Mode**
  
  | Work mode       | Description                                      | Peak (mA) |
  |-----------------|--------------------------------------------------|-----------|
  | TX              | 802.11b, 20 MHz, 1 Mbps @19 dBm                | 302       |
  |                 | 802.11g, 20 MHz, 54 Mbps @17.5 dBm             | 264       |
  | Active (RF working) | 802.11n, 20 MHz, MCS7, @16.5 dBm               | 257       |
  |                 | 802.11n, 40 MHz, MCS7, @16.5 dBm              | 267       |
  | RX              | 802.11b/g/n, 20 MHz                              | 77        |
  |                 | 802.11n, 40 MHz                                 | 81        |

- **Note:**
  - The current consumption measurements are taken with a 3.3 V supply at 25 °C of ambient temperature at the RF port. All transmitters' measurements are based on 100% duty cycle.
  - The current consumption figures in RX mode are for cases where the peripherals are disabled and the CPU idle.

---

#### Subsection: 
**5.4.2 Current Consumption in Other Modes**

The measurements below are applicable to ESP32-S2, ESP32-S2FH2, and ESP32-S2FH4. Since ESP32-S2FN4R2 and ESP32-S2R2 come with in-package PSRAM, their current consumption might be higher.

---

**Footer:**
- Espressif Systems
- Page 18 of ESP32-S2-MINI-2 & MINI-2U Datasheet v1.3

[Submit Documentation Feedback](#)