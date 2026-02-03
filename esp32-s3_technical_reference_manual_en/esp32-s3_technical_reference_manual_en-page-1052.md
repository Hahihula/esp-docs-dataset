**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Header:**
Table 28.9-3. Data-Fetching Control in PDM Mode

**Table Description and Content:**

1. **Data-Fetching Control Options Table:**
   - Columns:
     - "Mode"
     - "I2S_TX_MONO" (with values '0' or 'x')
     - "I2S_TX_Mono_FST_VLD" with a value of 1
   - Rows describe different data-fetching control requests to DMA in stereo and mono modes.

**Body Text:**
In PDM mode, I2Sn channel mode is controlled by `I2S_TX_CHAN_MOD` and `I2S_TX_WS_IDLE_POL`, see the table below.
- In PDM master mode, the WS level of I2Sn module is controlled by `I2S_TX_WS_IDLE_POL`. The frequency of WS signal is half of BCK frequency. The configuration of WS signal is similar to that of BCK signal.

**Subsection Title:**
Table 28.9-4. I2Sn Channel Control in PDM Mode

**Channel Control Operation Table:**

1. **Columns:** 
   - "Channel"
   - "Left Channel" (with options like `Stereo mode`, `Mono mode`)
   - "Right Channel" with operations
   - "Mode Control Field 1, Select Bit 2"

2. **Rows describe different control modes for stereo and mono channels:**
   - Transmit the left channel data.
   - Transmit the right channel data.

**Additional Information in Body Text:**
ESP32-S3 I2S0 also supports PCM-to-PDM output mode, where the PCM data from DMA is converted to PDM data. Configure `I2S_PCM2PDM_CONV_EN` to enable this mode.

**Footer:**
Espressif Systems
1052 ESP32-S3 TRM (Version 1.7)