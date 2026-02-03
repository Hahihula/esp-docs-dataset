**Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Subtitle:**
Register 37.4, RMT_CHm CONF0_REG (m = 4, 5, 6, 7) (0x0030, 0x0038, 0x0040, 0x0048)

**Table:**
- **Columns:** 
  - Offset
  - Name
  - Description

| Offset | Name                   | Description                                                                 |
|--------|------------------------|-----------------------------------------------------------------------------|
| 31     | (reserved)            |                                                                            |
| 30     | RMT_CARRIER_OUT_LV_CHm| RMT_CARRIER_EN_EN_CHm (reserved for m:4-6)                               |
| 29     | RMT_CARRIER_EN_CHm    |                                                                            |
| 28     | RMT_MEM_SIZE_CHm      |                                                                            |
| 27     | RMT_DMA_ACCESS_EN_CH7 | DMA access enable bit for channel 7. (R/W)                                |
|        |                       |                                                                            |
| 24-23 | RMT_IDLE_THRES_CHm   | This field is used to configure RX threshold. When no edge is detected on the input signal for continuous clock cycles longer than this field value, the receiver stops receiving data. (R/W) |
| 0      |                        |                                                                            |

**Body Text:**
- **Field Description:** RMT_DIV_CNT_CHm
  - This field is used to configure the clock divider of channel m.
  - Access type: Read/Write

- **Field Description:** RMT_IDLE_THRES_CHm
  - This field is used to configure RX threshold. When no edge is detected on the input signal for continuous clock cycles longer than this field value, the receiver stops receiving data.

- **Field Description:** RMT_DMA_ACCESS_EN_CH7 (Reserved for channel 4 - 6)
  - DMA access enable bit for channel 7.
  - Access type: Read/Write

- **Field Description:** RMT_MEM_SIZE_CHm
  - This field is used to configure the maximum number of memory blocks allocated to channel m.

- **Field Description:** RMT_CARRIER_EN_CHm
  - This is the carrier demodulation enable-bit for channel m.
    - Value: 
      - `1`: Enable carrier demodulation for input signal. O: disable carrier modulation for input signal (R/W)
  
- **Field Description:** RMT_CARRIER_OUT_LV_CHm
  - This bit is used to configure the position of carrier demodulation for channel m.
    - Values:
      - `1'h0`: Demodulate low-level carrier wave. 
      - `1'h1`: Demodulate high-level carrier wave.

**Footer:**
- Page number and document version information
  - "Espressif Systems"
  - "ESP32-S3 TRM (Version 1.7)"
  - "Submit Documentation Feedback"