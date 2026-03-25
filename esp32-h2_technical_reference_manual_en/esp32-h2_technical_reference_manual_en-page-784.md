

```markdown
Legend to state flow:

- `—`: corresponding state condition is not satisfied; repeats current state.
- `—·`: corresponding registers are set and conditions are satisfied; goes to next state.
- `-`: state registers are not set; skips one or more following states, depending on the registers of the following states are set or not.

Explanation to the conditions listed in the figure above:

• CONF condition: gpc[17:0] >= SPI_CONF_BITLEN[17:0]
• PREP condition: gpc[4:0] >= SPI_CS_SETUP_TIME[4:0]
• CMD condition: gpc[3:0] >= SPI_USR_COMMAND_BITLEN[3:0]
• ADDR condition: gpc[4:0] >= SPI_USR_ADDR_BITLEN[4:0]
• DUMMY condition: gpc[7:0] >= SPI_USR_DUMMY_CYCLELEN[7:0]
• DOUT condition: gpc[17:0] >= SPI_MS_DATA_BITLEN[17:0]
• DIN condition: gpc[17:0] >= SPI_MS_DATA_BITLEN[17:0]
• DONE condition: (gpc[4:0] >= SPI_CS_HOLD_TIME[4:0] || SPI_CS_HOLD == 1'b0)

A counter (gpc[17:0]) is used in the state machine to control the cycle length of each state. The states CONF, PREP, CMD, ADDR, DUMMY, DOUT, and DIN can be enabled or disabled independently. The cycle length of each state can also be configured independently.

29.5.9.2 Register Configuration for State and Bit Mode Control

Introduction

The registers, related to GP-SPI2 state control, are listed in Table 29.5-7. Users can enable QPI mode for GP-SPI2 by setting the bit SPI_QPI_MODE in register SPI_USER_REG.

Table 29.5-7. Registers Used for State Control in 1/2/4-bit Modes

| State | Control Registers for 1-bit Mode FSPI Bus                                                                 | Control Registers for 2-bit Mode FSPI Bus                                                                 | Control Registers for 4-bit Mode FSPI Bus                                                                 |
|-------|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| CMD   | SPI_USR_COMMAND_VALUE<br>SPI_USR_COMMAND_BITLEN<br>SPI_USR_COMMAND                                           | SPI_USR_COMMAND_VALUE<br>SPI_USR_COMMAND_BITLEN<br>SPI_FCMD_DUAL<br>SPI_USR_COMMAND                          | SPI_USR_COMMAND_VALUE<br>SPI_USR_COMMAND_BITLEN<br>SPI_FCMD_QUAD<br>SPI_USR_COMMAND                         |
| ADDR   | SPI_USR_ADDR_VALUE<br>SPI_USR_ADDR_BITLEN<br>SPI_USR_ADDR                                                  | SPI_USR_ADDR_VALUE<br>SPI_USR_ADDR_BITLEN<br>SPI_USR_ADDR<br>SPI_FADDR_DUAL                                  | SPI_USR_ADDR_VALUE<br>SPI_USR_ADDR_BITLEN<br>SPI_USR_ADDR<br>SPI_FADDR_QUAD                                 |
| DUMMY  | SPI_USR_DUMMY_CYCLELEN<br>SPI_USR_DUMMY                                                                   | SPI_USR_DUMMY_CYCLELEN<br>SPI_USR_DUMMY                                                                     | SPI_USR_DUMMY_CYCLELEN<br>SPI_USR_DUMMY                                                                     |
| DIN    | SPI_USR_MISO<br>SPI_MS_DATA_BITLEN                                                                         | SPI_USR_MISO<br>SPI_MS_DATA_BITLEN<br>SPI_FREAD_DUAL                                                       | SPI_USR_MISO<br>SPI_MS_DATA_BITLEN<br>SPI_FREAD_QUAD                                                      |
```