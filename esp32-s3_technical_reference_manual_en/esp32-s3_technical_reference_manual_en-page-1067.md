**Title:**
Chapter 28 I2S Controller (I2S)

**GoBack Link:** [GoBack](#)

---

**Subtitle: Register 28.10. I2S_RX_TDM_CTRL_REG (0x0050)**

Continued from the previous page...

- **I2S_RX_TDM_CHAN14_EN**
  - Description:
    ```
    Enable the valid data input of I2S RX TDM channel 14.
    0: Disable. Channel 14 only inputs O. (R/W)
    ```

- **I2S_RX_TDM_CHAN15_EN**
  - Description:
    ```
    Enable the valid data input of I2S RX TDM channel 15.
    0: Disable. Channel 15 only inputs O. (R/W)
    ```

- **I2S_RX_TDM_TOT_CHAN_NUM**
  - Description:
    ```
    The total number of channels in use in I2S RX TDM mode.
    Total channel number in use = this value + 1. (R/W)
    ```

**Subtitle: Register 28.11. I2S_RXEOF_NUM_REG (0x0064)**

- **I2S_RX_EOF_NUM**
  - Description:
    ```
    The bit length of RX data is (I2S_RX BITS_MOD + 1) * (I2S_RX_EOF_NUM + 1).
    Once the length of received data reaches such bit length, an in相处eof interrupt is triggered
    in the configured DMA RX channel. (R/W)
    ```

---

**Footer:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)