**Title:**
Chapter 27 I2C Controller (I2C)

**Subtitle:**
27.3 I2C Architecture

**Diagram Labels and Descriptions for Figure 27.3-1:**

- **APB_CLK domain**: 
  - cmd_rd, cmd0, cmd1, ..., cmd7
  - cmd_content
  
- **I2C_SCL domain**:
  - I2C TRANS START
  
- **CMD_Controller**:
  - SCL_LOW_PERIOD
  - SCL_HIGH_PERIOD
  - SCL_WAIT_HIGH_PERIOD
  - SCL_START_HOLD_TIME
  - SCL_STOP_HOLD_TIME

- **32x8bits**: 
  - r/w
  
- **TX RAM**
  
- **SCL_FSM**:
  - SCL_MAIN FSM
  
- **SDA**: 
  
- **DATA_Shifter**:
  - rdata/wdata
  
- **I2C_RX_LSB_FIRST, I2C_TX_LSB_FIRST**

**Diagram Labels and Descriptions for Figure 27.3-2:**
  
- APB BUS
- TX RAM (32x8bits)
- RX RAM (32x8bits)

**Text Explanation under Figures:**

The text explains that the architecture of an I2C master is shown in **Figure 27.3-1**, and a slave's structure can be seen from Figure 27.3-2.

**List Items for Master Architecture Components mentioned below each figure (in Markdown format):**
- transmit and receive memory (TX/RX RAM)
- command controller (CMD_Controller)
- SCL clock controller (SCL_FSM)

**Footer Information:**

Espressif Systems
986

Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)