**Title: Functional Description**

---

### **4.3.3 Bluetooth LE**

This subsection describes the chip’s Bluetooth capabilities, which facilitate wireless communication for low-power, short-range applications.

#### 4.3.3.1 Bluetooth LE PHY

Bluetooth Low Energy PHY in ESP32-C5 supports:

- 1 Mbps PHY
- 2 Mbps PHY for higher data rates
- coded PHY for longer range (125 Kbps and 500 Kbps)
- HW listen before talk (LBT)

#### **4.3.3.2 Bluetooth LE Link Controller**

Bluetooth Low Energy Link Controller and Host in ESP32-C5 support:

- direction finding (AoA/AoD)
- periodic advertising with responses (PAwR)
- LE connection subrating (LE enhanced connection update)
- LE advertising extensions and multiple advertising sets
- allow devices to operate in Broadcaster, Observer, Central, and Peripheral roles concurrently
- adaptive frequency hopping and channel assessment
- LE channel selection algorithm #2
- LE power control
- advertising coding selection
- encrypted advertising data
- LE GATT security levels characteristic
- AdvDataInfo in periodic advertising
- LE channel classification
- enhanced attribute protocol
- advertising channel index
- GATT caching
- periodic advertising sync transfer
- high duty cycle non-connectable advertising
- LE data packet length extension
- LE secure connections
- LE privacy 1.2

---

**Footer:**
Espressif Systems  
ESP32-C5 Series Datasheet v1.0  

[Submit Documentation Feedback](#)