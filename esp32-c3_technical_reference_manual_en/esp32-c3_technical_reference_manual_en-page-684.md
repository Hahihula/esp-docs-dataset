

```markdown
I2C_SCL_MAIN_ST_TO_INT interrupt is triggered, and then SCL_MAIN FSM goes to idle state. The value of I2C_SCL_MAIN_ST_TO_I2C should be less than or equal to 22, which means SCL_MAIN FSM could remain unchanged for 2^22 I2C_SCLK clock cycles at most before the interrupt is generated.

Timeout control for SCL is enabled by setting I2C_TIME_OUT_EN. When the level of SCL remains unchanged for more than 2^I2C_TIME_OUT_VALUE clock cycles, an I2C_TIME_OUT_INT interrupt is triggered, and then the I2C bus goes to idle state.
```

## 28.4.9 Command Configuration

When the I2C controller works in master mode, CMD_Controller reads commands from 8 sequential command registers and controls SCL FSM and SCL_MAIN FSM accordingly.

| cmd0 | 31       | 30:14    | 13:11    | 10   | 9     | 8           | 7:0         |
|------|----------|----------|----------|------|-------|-------------|-------------|
|      | CMD_DONE | reserved | op_code  | ack_value | ack_exp | ack_check_en | byte_num |

| cmd7 | 31       | 30:14    | 13:11    | 10   | 9     | 8           | 7:0         |
|------|----------|----------|----------|------|-------|-------------|-------------|
|      | CMD_DONE | reserved | op_code  | ack_value | ack_exp | ack_check_en | byte_num |

Figure 28.4-2. Structure of I2C Command Registers

Command registers, whose structure is illustrated in Figure 28.4-2, are active only when the I2C controller works in master mode. Fields of command registers are:

1. **CMD_DONE**: Indicates that a command has been executed. After each command has been executed, the CMD_DONE bit in the corresponding command register is set to 1 by hardware. By reading this bit, software can tell if the command has been executed. When writing new commands, this bit must be cleared by software.

2. **op_code**: Indicates the command. The I2C controller supports five commands:

    * RSTART: op_code = 6. The I2C controller sends a START bit or a RSTART bit defined by the I2C protocol.
    * WRITE: op_code = 1. The I2C controller sends a slave address, a register address (only in double addressing mode) and data to the slave.
    * READ: op_code = 3. The I2C controller reads data from the slave.
    * STOP: op_code = 2. The I2C controller sends a STOP bit defined by the I2C protocol. This code also indicates that the command sequence has been executed, and the CMD_Controller stops reading commands. After restarted by software, the CMD_Controller resumes reading commands from command register 0.
    * END: op_code = 4. The I2C controller pulls the SCL line down and suspends I2C communication. This code also indicates that the command sequence has completed, and the CMD_Controller stops executing commands. Once software refreshes data in command registers and the RAM, the CMD_Controller can be restarted to execute commands from command register 0 again.
```