**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Register Information:**
- Register Name: I2C_CTR_REG
- Register Address: Ox0004

**Table Description and Values for Each Bit in the Register:**

1. **I2C_SDAFORCE_OUT**: Configures the SDA output mode.
   - 0: Open drain output (R/W)
   - 1: Direct output
  
2. **I2C_SCLFORCE_OUT**: Configures the SDL output mode.
   - 0: Open drain output
   - 1: Direct output

3. **I2C_SAMPLE_SCL_LEVEL**: This bit is used to select the sampling mode for SCL level detection (R/W).
   - 0: Samples SDA data on high; 
   - 1: Samples SDA data on low.

4. **I2C_RXFULL_ACK_LEVEL**: This bit is used to configure the ACK value that needs to be sent by master when I2C_RXIFO_CNT has reached threshold (R/W).

5. **I2C_MS_MODE**: Set this bit to configure the I2C controller as an I2C Master; Clear it for slave configuration.
   - 0: Configure as Slave
   - 1: Configure as Master

6. **I2CTransStart**: This bit is used to start sending data in TX FIFO (WT).

7. **I2C_TX_LSB_FIRST**: This field controls the order of bits sent during transmission; sends from most significant.
   - 0: Sends least significant first
   - 1: Sends most significant first

8. **I2C_RX_LSB_FIRST**: This bit is used to control receiving data in RX FIFO (WT).
   - 0: Receives least significant first
   - 1: Receives most significant first

9. **I2C_CLK_EN**: Controls APB_CLK clock gating; always on.
   - 0: APB_CLK gated for power saving
  
10. **I2C_ARBITRATION_EN**: Enable bit for I2C bus arbitration function (R/W).
  
11. **I2C_FSM_RST**: Used to reset the SCL FSM when needed.

12. **I2C_CONF_UPGATE**: Synchronization control.
   - 0: No synchronization
   - 1: Synchronize
  
13. **I2C_SLV_TX_AUTO_START_EN**: Enable bit for slave automatic data transmission (R/W).
  
14. **I2C_ADDR_10BIT_RW_CHECK_EN**: Enable check if R/W is consistent with I2C protocol.
   - 0: No check
   - 1: Check
  
15. **I2C_ADDR_BROADCASTING_EN**: Enable bit for enabling broadcast addressing (R/W).

**Footer Information:**
- Document Title: ESP32-S3 TRM (Version 1.7)
- Page Number: 1022

**Navigation Links:**
- GoBack
- Submit Documentation Feedback