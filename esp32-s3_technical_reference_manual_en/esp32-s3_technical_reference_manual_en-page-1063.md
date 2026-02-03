**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Navigation Link:**
GoBack

---

**Continued from previous page...**

- **Register Description and Values for Chapter 28.5, I2S_RX_CONF_REG (0x0020):**
  - `I2S_RX_TDM_EN`:
    - Value: 1
    - Description: Enable I2S TDM RX mode.
    - Access Rights: Read/Write

  - `I2S_RX_PDM_EN`:
    - Value: 1
    - Description: Enable I2S PDM RX mode.
    - Access Rights: Read/Write

  - `I2S_RX_PDM2PCM_EN (for I2S0 only)`:
    - Value: 1
    - Description: Enable PDM-to-PCM RX mode. 
    - Access Rights: Disable or Enable PDM-to-PCM RX mode.

  - `I2S_RX_PDM_SINC_DSR_16_EN (for I2S0 only)`:
    - Description: Configure the down sampling rate of PDM RX filter group1 module.
      - Values and their descriptions are as follows, with corresponding bit positions in a register diagram provided below each description:

        | Bit Position | Value |
        |--------------|-------|
        | 31          | O     |
        | 29          | Xf    |
        | 28          | Oxf   |
        | 24-0        | Reset |

**Register Diagram:**
```
(reserved)
I2S_RX_SHIFT
I2S_RX_TDM_CHAN BITS
I2S_RX_HALF_BITS
I2S_RXBITS_MOD
I2S_RXDIV_NUM

31    30   29   28   24-0      18     17    16    15    13    12    7    6    0    Reset
```

**Register Descriptions:**

- `I2S_RX_TDM_WS_WIDTH`:
  - Description: The width of rx_ws_out (WS default level) in TDM mode is `(I2S_RX_TDM_WS_WIDTH + 1) * T_BCK`.
  - Access Rights: Read/Write

- `I2S_RX_BCK_DIV_NUM`:
  - Description: Configure the divider of BCK in RX mode.
  - Note: This divider must not be configured to 1.

- `I2S_RX BITS_MOD`:
  - Description: Validate data bit length for I2S RX channel. 
    - Values and their descriptions are as follows:

      | Value | Description |
      |-------|-------------|
      | 7     | All valid channel data is in 8-bit mode. |
      | 15    | All the valid channel data is in 16-bit mode. |
      | 23    | All the valid channel data is in 24-bit mode. |
      | 31    | All the valid channel data is in 32-bit mode.

- `I2S_RX_HALF_SAMPLE BITS`:
  - Description: I2S RX half sample bits.
  - Note: This value x 2 equals to BCK cycles in one WS period, with access rights Read/Write

- `I2S_RX_TDM_CHAN BITS`:
  - Description: Configure RX bit number for each channel in TDM mode. 
  - Bit number expected = this value + 1.

- `I2S_RX_MSB_SHIFT`:
  - Description: Control the timing between WS signal and MSB of data.
    - Values:

      | Value | Description |
      |-------|-------------|
      | O     | Align at rising edge. |

---

**Footer Information:**
Espressif Systems
1063 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback