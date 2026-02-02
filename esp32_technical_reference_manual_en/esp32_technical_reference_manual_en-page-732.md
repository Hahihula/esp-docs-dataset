**Title: Chapter 30 Remote Control Peripheral (RMT)**

**Register Name and Address Information**
- **Register**: RMT_CHnCONF1_REG (n = 0-7) (0x0024+8*n)
- **Address Bits**: 
  - [bit 31] Reserved
  - [bits 20 to 16] RMT_IDLE_OUT_EN_CHn
  - [bits 15 and below] Various control bits for different functionalities

**Control Bits Description**
- `RMT_IDLE_OUT_EN_CHn`: This is the output enable-control bit for channel n in IDLE state. (R/W)
- `RMT_IDLE_OUT_LV_CHn`: This bit configures the level of output signals in channel n when the latter is in IDLE state. (R/W)
- `RMT_REF_ALWAYS_ON_CHn`: This bit used to select the channel's base clock.
  - 1: clk_apb;
  - 0: clk_ref; (R/W)
- `RMT_REF_CNT_RST_CHn`: Setting this bit resets the clock divider of channel n. (R/W)
- `RMT_RX_FILTER_THRES_CHn`: In receive mode, channel n ignores input pulse when the pulse width is smaller than this value in APB clock periods.
  - Number indicates that it's a percentage or specific time unit; exact meaning not specified here but implied to be related to timing thresholds. (R/W)
- `RMT_RX_FILTER_EN_CHn`: This is receive filter’s enable-bit for channel n. (R/W)
- `RMT_TX_CONTI_MODE_CHn`: If this bit is set, instead of going into an idle state when transmission ends, the transmitter will restart transmission.
  - This results in a repeating output signal. (R/W)
- `RMT_MEM_OWNER_CHn`: This bit marks channel n’s RAM block ownership; Number indicates that it's likely related to memory allocation or usage control within specific channels and blocks of memory management system context but exact meaning not specified here, implied by the term "ownership".
  - While O indicates transmitter using RAM. (R/W)
- `RMT_MEM_RD_RST_CHn`: Set this bit to reset the read-RAM address for channel n by accessing the transmitter.
  - This is likely related memory management control within specific channels and blocks of memory but exact meaning not specified here, implied contextually as a reset function in RAM addressing. (R/W)
- `RMT_MEM_WR_RST_CHn`: Set this bit to reset the write-RAM address for channel n by accessing the receiver.
  - This is likely related memory management control within specific channels and blocks of memory but exact meaning not specified here, implied contextually as a reset function in RAM addressing. (R/W)
- `RMT_RX_EN_CHn`: Set this bit to enable receiving data on channel n; implies enabling or disabling the receiver functionality for that particular channel.
  - This is likely related communication control within specific channels and blocks of memory but exact meaning not specified here, implied contextually as a receive function. (R/W)
- `RMT_TX_START_CHn`: Set this bit to start sending data on channel n; implies enabling or disabling the transmitter functionality for that particular channel.
  - This is likely related communication control within specific channels and blocks of memory but exact meaning not specified here, implied contextually as a transmit function. (R/W)

**Footer**
- **Company**: Espressif Systems
- **Document Version**: ESP32 TRM (Version 5.6)
- **Page Number**: 732

**Navigation Links**
- Submit Documentation Feedback