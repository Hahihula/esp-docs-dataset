**Chapter Title:**
Chapter 21 I2C Controller (I2C)

**Section Header:**
GoBack

**Subsection Titles and Content:**

- **I2C_SCL_**
  - LOW_PERIOD_REG registers are used to configure the frequency and duty cycle of the signal on the SCL line.

- **SDA_FSM:**
  - A state machine that controls the SDA data line.
  
- **DATA_Shifter:**
  - Converts byte data into an outgoing bitstream, or converts an incoming bitstream to byte data. I2C_RX_LSB_FIRST and I2C_TX_LSB_FIRST can be used for configuring whether the LSB or MSB is stored or transmitted first.

- **SCL_Filter and SDA_Filter:**
  - Input noise filter for the I2C Slave.
  - The filter can remove line glitches with pulse width less than I2C_SCL_FILTER_THRES and I2C_SDA_FILTER_THRES ABP clock cycles. It can be enabled or disabled by configuring I2C_SCL_FILTER_EN and I2C_SDA_FILTER_EN.

**Subsection Title:**
21.3.3 I2C Bus Timing

**Image Description with Caption:**
- **Figure 21.3-3:** An illustration of an I2C sequence chart.
  
**Caption for Image:**
- Figure caption is "I2C Sequence Chart."

**Text Explanation under the image:**
- Describes how SCL operates in master and slave modes, assigns values to registers based on mode.

**Table Title with Description:**
- **Table 21.3-1:** I2C Frequency Configuration

**Table Content Summary (in Markdown format):**

| I2C_SCL_SCL_FILTER_EN | I2C_SCL_FILTER_THRES | SCL_Low_Level_Cycles | SCL_High_Level_Cycles |
|------------------------|-----------------------|----------------------|-----------------------|
| 0                      | Don't care            | I2C_SCL_HIGH_PERIOD+7
                          | (I2C_SCL_HIGH_PERIOD+8) |
| 1                      | [0,2]                 | I2C_SCL_LOW_PERIOD+1 |                   |

**Equation:**
- \( f_{ scl } = \frac{SCL\_Low\_Level\_Cycles + SCL\_High\_Level\_Cycles}{80 MHz} \)

**Text Explanation under the table and equation:**
- Describes how data transmission works in I2C protocol, starting with a START condition ending with a STOP. Data is transmitted one byte at time.

**Footer Information:**
- "Espressif Systems"
- Page number 391
- Document version (Version 5.6)
- Link to submit documentation feedback