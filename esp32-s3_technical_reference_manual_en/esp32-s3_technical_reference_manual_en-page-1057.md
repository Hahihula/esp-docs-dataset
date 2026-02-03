**Title: Chapter 28 I2S Controller (I2S)**

---

### Table Title:
Table 28.10-3. Channel Storage Data Endian

| Channel | Storage | Origin Data | Endian of Processed Data | I2S_RX_BIG_ENDIAN |
|---------|---------|-------------|--------------------------|--------------------|
|         |         |             |                         |                    |
| Data Width | {B3, B2, B1, BO} | {BO, B1, B2, B3} | 0                     |                      |
|          |         |             |                         |                    |
|          |         |             |                         |                    |
|          |         |             |                         |                    |

---

**Subtitle: A-law/μ-law Compression and Decompression**

ESP32-S3 I2Sn compresses/decompresses the data to be stored in 32-bit by A-law or by μ-law. By default, zeros are filled to high bits.

Configure `I2S_RX_PCM_BYPASS` to:

- **0:** Compress or decompress the data.
- **1:** Do not compress or decompress the data.

Configure `I2S_RX_PCM_CONF` to:

- **0:** Decompress the data using A-law.
  - **1:** Compress the data using A-law.
  - **2:** Decompress the data using μ-law.
  - **3:** Compress the data using μ-law.

At this point, the data format control is complete. Data then is stored into memory via DMA.

---

**Subtitle: Software Configuration Process**

**Section Title: Configure I2Sn as TX Mode**

Follow the steps below to configure I2Sn as TX mode via software:

1. **Configure the clock as described in Section 28.6.**
2. **Configure signal pins according to Table 28.4-1.**
3. Select the mode needed by configuring the bit `I2S_TX_SLAVE_MOD`:
   - **0:** master TX mode
   - **1:** slave TX mode

4. Set needed TX data mode and TX channel mode as described in Section 28.9, and then set the bit `I2S_TX_UPDATE`.

5. Reset TX unit and TX FIFO as described in Section 28.7.

---

**Footer:**
Espressif Systems  
1057  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback