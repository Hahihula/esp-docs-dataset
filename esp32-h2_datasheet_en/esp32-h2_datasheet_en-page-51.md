**Title: Functional Description**

- **Coded PHY for longer range (125 Kbps and 500 Kbps)**
- HW Listen before talk (LBT)

---

### Section Title:
4.3.2.2 Bluetooth LE Link Controller

#### Body Text:

ESP32-H2’s Bluetooth Low Energy Link Controller supports:
- LE advertising extensions, to enhance broadcasting capacity and broadcast more intelligent data
- Multiple advertisement sets
- Simultaneous advertising and scanning
- Multiple connections in simultaneous central and peripheral roles
- Adaptive frequency hopping and channel assessment
- Channel selection algorithm #2
- LE power control
- Connection parameter update
- High duty cycle non-connectable advertising
- LE privacy 1.2
- LE data packet length extension
- Link layer extended scanner filter policies
- Low duty cycle connectable directed advertising
- Link layer encryption
- LE Ping

---

### Section Title:
4.3.3 802.15.4

#### Body Text:

ESP32-H2 includes an IEEE Standard 802.15.4 subsystem that integrates PHY and MAC layers. It supports various software stacks including Thread, Zigbee, Matter, HomeKit, MQTT, and so on.

---

### Subsection Title:
4.3.3.1 802.15.4 PHY

#### Body Text:

ESP32-H2’s 802.15.4 PHY supports:
- O-QPSK PHY in 2.4 GHz
- 250 Kbps data rate
- RSSI and LQI supported

---

### Subsection Title:
4.3.3.2 802.15.4 MAC

#### Body Text:

ESP32-H2 supports most key features defined in IEEE Standard 802.15.4-2015, includes:
- CSMA/CA
- Active scan and energy detect

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback ESP32-H2 Series Datasheet v1.2