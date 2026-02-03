**Title: Chapter 28 I2S Controller (I2S)**

---

### Register 28.19. I2S_TX_TIMING_REG (0x00C5)

| Field | Description |
|-------|-------------|
| **(reserved)** | Various reserved fields are listed with specific bit positions and values, such as `0x0` or `0xX`. |

- 31: Reserved
- 29 to 26: Reserved bits.
- 25 (I2S_TX_BCK_IN_DM): The delay mode of I2S TX BCK input signal. Options include bypassing, delaying by rising edge, and not used with read/write access.

| Field | Description |
|-------|-------------|
| **(reserved)** | Various reserved fields are listed with specific bit positions and values, such as `0x0` or `0xX`. |

- 24 to 16: Reserved bits.
- 15 (I2S_TX_WS_IN_DM): The delay mode of I2S TX WS input signal. Options include bypassing, delaying by rising edge.

| Field | Description |
|-------|-------------|
| **(reserved)** | Various reserved fields are listed with specific bit positions and values, such as `0x0` or `0xX`. |

- 14 to 9: Reserved bits.
- 8 (I2S_TX_WS_OUT_DM): The delay mode of I2S TX WS output signal. Options include bypassing.

---

### Register 28.20. I2SLC_HUNG_CONFIG_REG (0x0C60)

| Field | Description |
|-------|-------------|
| **(reserved)** | Various reserved fields are listed with specific bit positions and values, such as `0x0` or `0xX`. |

- 31: Reserved
- 29 to 8: Reserved bits.
- 7 (I2S_LC_FIFO_TIMEOUT): FIFO hung counter threshold. The tick counter is reset when the value exceeds a certain limit.

| Field | Description |
|-------|-------------|
| **(reserved)** | Various reserved fields are listed with specific bit positions and values, such as `0x0` or `0xX`. |

- 6 (I2S_LC_FIFO_TIMEOUT_SHFT): The enable bit for FIFO timeout. Options include read/write access.

---

**Footer:**
Espressif Systems  
1076  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)