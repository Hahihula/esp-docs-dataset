**Title: Chapter 28 I2S Controller (I2S)**

---

### Figure Caption:
- **Figure 28.9-3. PDM Channel Control**

| WS(LRCK) | Left Right |
|-----------|------------|
| SD(SDOUT)- | Data (Left) = Data (Right) |

**Code:**
```
I2S_TX_CHAN_MOD = 2; I2S_TX_WS_IDLE_POL = 1;
```

---

### Subtitle:
#### **28.10 Receiving Data**

**Note:** 
- Updating the configuration described in this and subsequent sections requires to set `I2S_RX_UPDATE` accordingly, to synchronize I2Sn RX registers from APB clock domain to RX clock domain.

For more detailed configuration, see Section 28.11.2

In RX mode, I2Sn first reads data from peripheral interface, and then stores the data into memory via DMA, according to the configured channel mode and data mode.


---

### Subtitle:
#### **28.10.1 Channel Mode Control**

**Body Text:**
- ESP32-S3 I2Sn supports both TDM RX mode and PDM RX mode.
  - Set `I2S_RX_TDM_EN` to enable TDM RX mode, or set `I2S_RX_PDM_EN` to enable PDM RX mode.

**Note:** 
- `I2S_RX_TDM_EN` and `I2S_RX_PDM_EN` must not be cleared or set simultaneously.


---

### Subtitle:
#### **28.10.1 I2Sn Channel Control in TDM Mode**

In TDM mode, I2Sn supports up to 16 channels to input data.
- The total number of RX channels in use is controlled by `I2S_RX_TDM_TOT_CHAN_NUM`.
  - For example: if `I2S_RX_TDM_TOT_CHAN_NUM` is set to 5,
    channel 0 ~ 5 will be used to receive data.

In these RX channels, if `I2S_RX_TDM_CHANn_EN` is set:
- **1:** This channel data is valid and will be stored into RX FIFO.
- **0:** This channel data is invalid and will not be stored into RX FIFO.

In TDM master mode, WS signal is controlled by
  - `I2S_RX_WS_IDLE_POL`
    - the default level of WS signal

**Code:**
```
I2S_RX_TDM_WS_WIDTH
```

---

### Footer:
- **Page Number:** 1054
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Link:** Submit Documentation Feedback