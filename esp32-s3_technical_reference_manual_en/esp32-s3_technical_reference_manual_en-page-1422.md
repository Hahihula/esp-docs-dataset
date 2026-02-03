**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Body Text:**

is set to 1, the receiver starts receiving data and stores the data to address 48 * m, and then to higher RAM address. When the receiver finishes storing the received data to (48 * (m + 1) - 1), the receiver continues receiving data and storing data to the address 48 * m again, no change is detected on a signal level for more than RMT_IDLE_THRES_CHm clock cycles. Wrap mode is also applicable for RMT_MEM_SIZE_CHm > 1.

An RMT_CHm_RX_THR_EVENT_INT interrupt is generated when the size of received pulse codes is larger than or equal to the value set by RMT_CHm_RX_LIM_REG. In wrap mode, RMT_CHm_RX_LIM_REG can be set to a half or a fraction of the size of the channel’s RAM block. When an RMT_CHm_RX_THR_EVENT_INT interrupt is detected, the already used RAM region can be updated by subsequent data.

**Subsection Title:**
37.3.5.3 RX Filtering

**Body Text:**

Users can enable the receiver to filter input signals by setting RMT_RX_FILTER_EN_CHm for channel m. The filter samples input signals continuously, and detects the signals which remain unchanged for a continuous RMT_RX FIL.

TER THRES CHm rmt_sclk cycles as valid; otherwise, the signals will be detected as invalid. Only the valid signals can pass through this filter. The filter removes pulses with a length of less than RMT_RX_FILTER_THRES_CHm rmt_sclk cycles.

**Subsection Title:**
37.3.5.4 RX Demodulation

**Body Text:**

Users can enable RX demodulation on input signals or on filtered signals by setting RMT_CARRIER_EN_CHm. RX demodulation can be applied to high-level carrier wave or low-level carrier wave, depending on the configuration of RMT_CARRIER_OUT_LV_CHm:

- 1: demodulate high-level carrier wave
- 0: demodulate low-level carrier wave

Users can configure RMT_CARRIER_HIGH_THRES_CHm and RMT_CARRIER_LOW_THRES_CHm to set the thresholds to demodulate high-level carrier or low-level carrier. If the high-level of a signal lasts for less than RMT_CARRIER_HIGH_THRES_CHm clk_div cycles, or the low-level lasts for less than RMT_CARRIER_LOW_THRES_CHm clk_div cycles, such level is detected as a carrier and then is filtered out.

**Subsection Title:**
37.3.6 Configuration Update

**Body Text:**

To update RMT registers configuration, please set RMT_CONF_UPDATE_CHn/m for each channel first. All the bits/fields listed in the second column of Table 37.3-1 should follow this rule.

**Table Title and Content:**
Table 37.3-1. Configuration Update

| Register | Bit/Field Configuration Update |
|----------|----------------------------------|
| TX Channel | RMT_CARRIER_OUT_LV_CHn, RMT_CARRIER_EN_CHn, RMT_CARRIEREFF_EN_CHn, RMT_DIV_CNT_CHn, RMT_TX_STOP_CHn, RMT_IDLE_OUT_EN_CHn, RMT_IDLE_OUT_LV_CHn |

**Footer:**
Espressif Systems
1422 ESP32-S3 TRM (Version 1.7)