

```markdown
#### 47.8.1.2 PDM RX Mode

In PDM RX mode, LP I2S converts the serial data from channels to the data to be entered into memory. LP I2S supports both PDM raw data reception and PDM-to-PCM data format conversion.

In PDM RX master mode, the default level of the WS signal is controlled by `LP_I2S_RX_WS_IDLE_POL`. WS frequency is half of the BCK frequency. The configuration of the BCK signal is similar to that of WS signal as described in Section 47.5. Note, in PDM RX mode, the value of `LP_I2S_RX_HALF_SAMPLE_BITS` must be same as that of `LP_I2S_RX_BITS_MOD`.

When the PDM-to-PCM converter is enabled for LP I2S, the received PDM data is converted to PCM data and controlled according to the data mode. Configure `LP_I2S_RX_PDM2PCM_EN` to enable this converter. The register configuration for PDM-to-PCM converter is as follows:

*   Configure sampling frequency and downsampling rate.

    When LP I2S PDM-to-PCM converter is enabled, PDM clock frequency is:

    -   in master mode: PDM clock frequency is equal to BCK frequency.
    -   in slave mode: PDM clock is provided by external device.

    The sampling frequency (`f_Sampling`) is related to PDM clock frequency as follows:

    ```latex
    f_{Sampling} = \frac{f_{PDM}}{DSR}
    ```

    Downsampling rate (DSR) is related to `LP_I2S_RX_PDM_SINC_DSR_16_EN` as follows:

    ```latex
    DSR = LP_I2S_RX_PDM_SINC_DSR_16_EN \times 64
    ```

    Configure the registers according to needed master/slave mode, sampling frequency, and downsampling rate.

*   Configure valid channels.

    When the PDM-to-PCM converter is enabled, input signals from eight channels are supported at most. See Table 47.8-1 for the register configuration and related channels.

**Table 47.8-1. PDM-to-PCM Data Input**

<table><thead><tr><td>Input Data Signal</td><td>Channel</td><td>Enable Register</td></tr></thead><tbody><tr><td rowspan="2">LP_I2SI_SD_in</td><td>Left channel</td><td>LP_I2S_RX_TDM_PDM_CHANO_EN</td></tr><tr><td>Right channel</td><td>LP_I2S_RX_TDM_PDM_CHAN1_EN</td></tr></tbody></table>

#### 47.8.2 Data Format Control

The data format of LP I2S is controlled in the following phases:

*   Phase I: Serial input data is converted into the data to be saved to RX FIFO;
*   Phase II: The data is read from RX FIFO and converted according to the input data mode.

##### 47.8.2.1 Bit Order Control of Channel Data

The channel data will be stored as the data to be input in order from high to low. The data bit order in each channel is controlled by `LP_I2S_RX_BIT_ORDER`:
```