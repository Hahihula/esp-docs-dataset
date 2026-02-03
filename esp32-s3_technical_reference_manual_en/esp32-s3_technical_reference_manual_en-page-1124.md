**Title: Chapter 30 SPI Controller (SPI)**

**Legend to state flow:**
- : indicates corresponding state condition is not satisfied; repeats current state.
- : corresponding registers are set and conditions are satisfied; goes to next state.

- : state registers are not set; skips one or more following states, depending on the registers of the following states are set or not.

**Explanation of the conditions listed in the figure above:**

- CONF condition: gpc[17:0] >= SPI_CONF_BITLEN [17:0]
- PREP condition: gpc[4:0] > = SPI_CS_SETUP_TIME [4:0]
- CMD condition: gpc[3:0] > = SPI_USR_COMMAND_BITLEN [3:0]
- ADDR condition: gpc[4:0] >= SPI_USR_ADDR_BITLEN [4:0]
- DUMMY condition: gpc[7:0] >= SPI_USR_DUMMY_CYCLELEN [7:0]
- DOUT condition: gpc[17:0] >= SPI_MS_DATA_BITLEN [17:0]
- DIN condition: gpc[17:0] > = SPI_MS_DATA_BITLEN [17:0]
- DONE condition: (gpc[4:0] >= SPI_CS_HOLD_TIME [4:0] || SPI_CS_HOLD == 1'b0)

A counter (gpc[17:0]) is used in the state machine to control the cycle length of each state. The states CONF, PREP, CMD, ADDR, DUMMY, DOT, and DIN can be enabled or disabled independently. The cycle length of each state can also be configured independently.

**Subtitle: 30.5.8.2 Register Configuration for State and Bit Mode Control**

**Introduction**
The registers related to GP-SPI state control are listed in Table 30.5-8. Users can enable QPI mode for GP-SPI by setting the bit SPI_QPI_MODE in register SPI_USER_REG.

**Footer:**
Espressif Systems
1124 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback