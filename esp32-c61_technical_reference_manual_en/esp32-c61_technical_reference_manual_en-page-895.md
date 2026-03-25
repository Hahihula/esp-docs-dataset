

```markdown
Chapter 26  SPI Controller (SPI)

Explanation of the conditions listed in the figure above:

*   CONF condition: gpc[17:0] >= SPI_CONF_BITLEN[17:0]
*   PREP condition: gpc[4:0] >= SPI_CS_SETUP_TIME[4:0]
*   CMD condition: gpc[3:0] >= SPI_USR_COMMAND_BITLEN[3:0]
*   ADDR condition: gpc[4:0] >= SPI_USR_ADDR_BITLEN[4:0]
*   DUMMY condition: gpc[7:0] >= SPI_USR_DUMMY_CYCLELEN[7:0]
*   DOUT condition: gpc[17:0] >= SPI_MS_DATA_BITLEN[17:0]
*   DIN condition: gpc[17:0] >= SPI_MS_DATA_BITLEN[17:0]
*   DONE condition: (gpc[4:0] >= SPI_CS_HOLD_TIME[4:0] || SPI_CS_HOLD == 1'b0)

A counter (gpc[17:0]) is used in the state machine to control the cycle length of each state. The states CONF, PREP, CMD, ADDR, DUMMY, DOUT, and DIN can be enabled or disabled independently. The cycle length of each state can also be configured independently.

26.5.9.2  Register Configuration for State and Bit Mode Control

Introduction

The registers, related to GP-SPI2 state control, are listed in Table 26.5-7. Users can enable QPI mode for GP-SPI2 by setting the bit SPI_QPI_MODE in register SPI_USER_REG.
```