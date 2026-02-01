**Title: Functional Description**

---

### **4.3.2.3 Networking Features**

Espressif provides libraries for TCP/IP networking, ESP-WIFI-MESH networking, and other networking protocols over Wi-Fi. TLS 1.0, 1.1 and 1.2 is also supported.

---

### **4.3.3 Bluetooth LE**

This subsection describes the chip’s Bluetooth capabilities, which facilitate wireless communication for low-power, short-range applications. ESP32-C6 includes a Bluetooth Low Energy subsystem that integrates a hardware link controller, an RF/modem block and a feature-rich software protocol stack. It supports the core features of Bluetooth 5 and Bluetooth mesh.

---

### **4.3.3.1 Bluetooth LE PHY**

Bluetooth Low Energy PHY in ESP32-C6 supports:

- 1 Mbps PHY
- 2 Mbps PHY for higher data rates
- Coded PHY for longer range (125 Kbps and 500 Kbps)
- HW listen before talk (LBT)

---

### **4.3.3.2 Bluetooth LE Link Controller**

Bluetooth Low Energy Link Controller in ESP32-C6 supports:

- LE Advertising Extensions, to enhance broadcasting capacity and broadcast more intelligent data
- Multiple advertising sets
- Simultaneous advertising and scanning
- Multiple connections in simultaneous central and peripheral roles
- Adaptive Frequency Hopping (AFH) and channel assessment
- LE Channel Selection Algorithm #2
- LE Power Control
- Connection parameter update
- High Duty Cycle Non-Connectable Advertising
- LE privacy 1.2
- LE Data Packet Length Extension
- Link Layer Extended Scanner Filter policies
- Low duty cycle directed advertising
- Link layer encryption
- LE Ping

---

**Footer:**
Espressif Systems  
ESP32-C6 Series Datasheet v1.4  

[Submit Documentation Feedback](#)