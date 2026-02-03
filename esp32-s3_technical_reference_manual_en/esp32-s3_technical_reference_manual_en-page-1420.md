**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Body Text with Code and Descriptions**

1. **Section Heading:** 
   - Subsection "37.3.4.2 Wrap TX Mode"
   
   **Content Description:**
   To transmit more pulse codes that can be fitted in the channel’s RAM, users can enable wrap mode by setting `RMT_MEM_TX_WRAP_EN_CHn`. In wrap mode, the transmitter sends data from RAM in loops till an end-marker is encountered.

   - Example Explanation:
     If `RMT_MEM_SIZE_CHn = 1`, then the transmitter starts sending data from address `(48 * n + r)`, and continues to send more until it reaches the last byte. Once done, if there are remaining bytes (from higher RAM addresses), they continue being sent.

   - Note:
     When `RMT_MEM_SIZE_CHn > 1`, wrap mode is applicable for sending data from a larger range of memory.
   
2. **Section Heading:**
   - Subsection "37.3.4.3 TX Modulation"
   
   **Content Description:**
   Transmitter output can be modulated with a carrier wave by setting `RMT_CARRIER_EN_CHn`. The duration for high and low levels is configurable.

   - Example Explanation:
     If the cycle length of the carrier (e.g., `RMT_CARRIER_HIGH_CHn + 1`) is set, it determines how long each level lasts. When `RMT_CARRIER_OUT_LV_CHn` = set, a certain signal pattern can be created by adding or subtracting from this base duration.

   - Note:
     The carrier wave's presence on all output signals (`0`) vs only valid pulse codes (`1`) is configurable via `RMT_CARRIEREFF_EN_CHn`.

3. **Section Heading:**
   - Subsection "37.3.4.4 Continuous TX Mode"
   
   **Content Description:**
   The continuous mode can be enabled by setting `RMT_TX_CONTINU_MODE_CHn`. In this configuration, the transmitter sends pulse codes from RAM in loops.

   - Example Explanation:
     If an end-marker is encountered (`0`), it starts transmitting again. No need for additional setup if no marker occurs.
   
4. **Footer:**
   Espressif Systems
   1420 ESP32-S3 TRM (Version 1.7)
   Submit Documentation Feedback