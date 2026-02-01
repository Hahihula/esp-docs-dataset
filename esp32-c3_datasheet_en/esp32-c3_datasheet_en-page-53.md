**Title: Functional Description**

---

### **4.3.2.3 Networking Features**

Espressif provides libraries for TCP/IP networking, ESP-WIFI-MESH networking, and other networking protocols over Wi-Fi. TLS 1.0, 1.1 and 1.2 is also supported.

---

### **4.3.3 Bluetooth LE**

This subsection describes the chip’s Bluetooth capabilities, which facilitate wireless communication for low-power, short-range applications. ESP32-C3 includes a Bluetooth Low Energy subsystem that integrates a hardware link layer controller, an RF/modem block and a feature-rich software protocol stack. It supports the core features of Bluetooth 5 and Bluetooth mesh.

---

### **4.3.3.1 Bluetooth LE PHY**

Bluetooth Low Energy radio and PHY in ESP32-C3 support:

- 1 Mbps PHY
- 2 Mbps PHY for higher data rates
- coded PHY for longer range (125 Kbps and 500 Kbps)
- HW Listen before talk (LBT)

---

### **4.3.3.2 Bluetooth LE Link Controller**

Bluetooth Low Energy Link Layer Controller in ESP32-C3 supports:

- LE advertising extensions, to enhance broadcasting capacity and broadcast more intelligent data
- multiple advertisement sets
- simultaneous advertising and scanning
- multiple connections in simultaneous central and peripheral roles
- adaptive frequency hopping and channel assessment
- LE channel selection algorithm #2
- connection parameter update
- high duty cycle non-connectable advertising
- LE privacy 1.2
- LE data packet length extension
- link layer extended scanner filter policies
- low duty cycle directed advertising
- link layer encryption
- LE Ping

---

**Footer:**
Espressif Systems  
ESP32-C3 Series Datasheet v2.2  

[Submit Documentation Feedback](#)