**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Header:**
28.10.1 Channel Control in PDM Mode

**Body Text:**

In PDM mode, `I2Sn` converts the serial data from channels to the data to be entered into memory.

In PDM master mode, the WS level of `I2Sn` module is controlled by `I2S_RX_WS_IDLE_POL`. WS frequency is half of BCK frequency. The configuration of BCK signal is similar to that of WS signal as described in Section 28.6. Note, In PDM RX mode, the value of `I2S_RX_HALF_SAMPLE BITS` must be same as that of `I2S_RXBITS_MOD`.

`I2SO` supports PDM-to-PCM input mode, in which the received PDM data is converted to PCM data and controlled according to the data mode. Configure `I2S_RX_PDM2PCM_EN` to enable this mode.

The register configuration for PDM-to-PCM input mode is as follows:

- Configure sampling frequency and downsampling rate.
  - In PDM-to-PCM input mode, PDM clock frequency is:
    - in master mode: PDM clock frequency is equal to BCK frequency
    - in slave mode: PDM clock is provided by external device.

The sampling frequency (`fSampling`) is related to PDM clock frequency as follows:

\[ f_{\text{Sampling}} = \frac{f_{\text{PDM}}}{DSR} \]

Downsampling rate (DSR) is related to `I2SO_RX_PDM_SINC_DSR_16_EN` as follows:
\[ DSR = I2SO_RX_PDM_SINC_DSR_16_EN \times 64 \]

Configure the registers according to needed master/slave mode, sampling frequency, and downsampling rate.

- Configure valid channels.
  - In PDM-to-PCM mode, input signals from eight channels are supported at most. See Table `28.10-1` for the register configuration and related channels.

**Table Title:**
Table 28.10-1. PDM-to-PCM Input Mode

| Input Data Signal | Channel       | Enable Register                   |
|-------------------|---------------|----------------------------------|
| I2SO1_Data_in     | Left channel  | `I2SO_RX_TDM_PDM_CHAN0_EN`       |
| I2SO1_Data_in     | Right channel | `I2SO_RX_TDM_PDM_CHAN1_EN`       |
| I2SO2_Data_in     | Left channel  | `I2SO_RX_TDM_PDM_CHAN2_EN`       |
| I2SO2_Data_in     | Right channel | `I2SO_RX_TDM_PDM_CHAN3_EN`       |
| I2SO3_Data_in     | Left channel  | `I2SO_RX_TDM_PDM_CHAN4_EN`       |
| I2SO3_Data_in     | Right channel | `I2SO_RX_TDM_PDM_CHAN5_EN`       |
| I2SO4_Data_in     | Left channel  | `I2SO_RX_TDM_PDM_CHAN6_EN`       |
| I2SO4_Data_in     | Right channel | `I2SO_RX_TDM_PDM_CHAN7_EN`       |

**Section Header:**
28.10.2 Data Format Control

**Body Text:**

Data format is controlled in the following phases:

Espressif Systems

**Footer Information:**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback