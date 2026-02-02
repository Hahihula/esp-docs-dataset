**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Register Information:**

- **Register Name:** Register 22.33, I2S_PDM_CONF_REG (0x00b4)
  
  - **Field Descriptions and Values in Hexadecimal:**
    ```
    31  26  25  24  23  22  21  20  19  18  17  16   15     8      7       6
    (reserved) I2S_TX_PDM_HP_SINC_DELTA_IN_SHIFT I2S_TX_PDM_HP_IN_SHIFT I2S_TX_PDM_SINC_EN I2S_TX_PDM_SINCdelta_EN I2S_TX_PDM_SINCdelta_IN SHIFT I2S_TX_PDM_SINCdelta_IN SHIFT I2S_TX_PDM_SINCdelta_IN SHIFT
    0   0   0   1   0x1 OX1 OX1 OX1 OX1 OX1 OX1 OX1 OX1 OX1 Reset
    ```

- **Field Descriptions:**
  - `I2S_TX_PDM_HP_BYPASS`: Set this bit to bypass the transmitter's PDM HP filter. (R/W)
  - `I2S_RX_PDM_SINC_DSR_16_EN`: PDM downsampling rate for filter group 1 in receiver mode. (R/W) 
    ```
    1: downsampling rate = 128;
    0: downsampling rate = 64.
    ```
  - `I2S_TX_PDM_SIGMADELTA_IN_SHIFT`: Adjust the size of the input signal into filter module. (R/W)
    ```
    O: divided by 2; 1: multiplied by 1; 2: multiplied by 2; 3: multiplied by 4.
    ```
  - `I2S_TX_PDM_SINC_IN_SHIFT`: Adjust the size of the input signal into filter module. (R/W)
    ```
    O: divided by 2; 1: multiplied by 1; 2: multiplied by 2; 3: multiplied by 4.
    ```
  - `I2S_TX_PDM_LP_IN_SHIFT`: Adjust the size of the input signal into filter module. (R/W)
    ```
    O: divided by 2; 1: multiplied by 1; 2: multiplied by 2; 3: multiplied by 4.
    ```
  - `I2S_TX_PDM_HP_IN_SHIFT`: Adjust the size of the input signal into filter module. (R/W)
    ```
    O: divided by 2; 1: multiplied by 1; 2: multiplied by 2; 3: multiplied by 4.
    ```

- **Additional Fields and Descriptions:**
  - `I2S_TX_PDM_SINC_OSR2`: Upsampling rate = 64x2s_tx_pdm_sinc_osr2 (R/W)
  - `I2S_PDM2PCM_CONV_EN`: Set this bit to enable PDM-to-PCM converter. (R/W)
  - `I2S_PCM2PDM_CONV_EN`: Set this bit to enable PCM-to-PDM converter. (R/W)

- **Register Name:** Register 22.34, I2S_PDM_FREQ_CONF_REG (0x00b8)

  - **Field Descriptions and Values in Hexadecimal:**
    ```
    31   20  19     18      17       16        15         10          9           8
    (reserved) I2S_TX_PDM_FP I2S_TX_PDM_FS Reset
    ```

- **Field Descriptions:**
  - `I2S_TX_PDM_FP`: PCM-to-PDM converter's PDM frequency parameter. (R/W)
  - `I2S_TX_PDM_FS`: PCM-to-PDM converter's PCM frequency parameter. (R/W)

**Footer Information:**
- "Espressif Systems"
- Page number and document version:
  ```
  ESP32 TRM (Version 5.6) 
  Submit Documentation Feedback
  ```