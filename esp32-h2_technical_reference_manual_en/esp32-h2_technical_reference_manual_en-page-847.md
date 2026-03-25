

```markdown
## 30.4.8 Timeout Control

The I2C controller has three types of timeout control, namely timeout control for SCL_FSM, SCL_MAIN_FSM, and the SCL line. The first two are always enabled, while the third is configurable.

When SCL_FSM remains unchanged for more than `2^I2C_SCL_ST_TO_I2C` clock cycles, an I2C_SCL_ST_TO_INT interrupt is triggered, and then SCL_FSM goes to idle state. The value of `I2C_SCL_ST_TO_I2C` should be less than or equal to 22, which means SCL_FSM could remain unchanged for `2^22` I2C_SCLK clock cycles at most before the interrupt is generated.

When SCL_MAIN_FSM remains unchanged for more than `2^I2C_SCL_MAIN_ST_TO_I2C` I2C_SCLK clock cycles, an I2C_SCL_MAIN_ST_TO_INT interrupt is triggered, and then SCL_MAIN_FSM goes to idle state. The value of `I2C_SCL_MAIN_ST_TO_I2C` should be less than or equal to 22, which means SCL_MAIN_FSM could remain unchanged for `2^22` clock cycles at most before the interrupt is generated.

Timeout control for SCL is enabled by setting I2C_TIME_OUT_EN. When the level of SCL remains unchanged for more than `2^I2C_TIME_OUT_VALUE` clock cycles, an I2C_TIME_OUT_INT interrupt is triggered, and then the I2C bus goes to idle state.

## 30.4.9 Command Configuration

When the I2C controller works in master mode, CMD_Controller reads commands from 8 sequential command registers and controls SCL_FSM and SCL_MAIN_FSM accordingly.

Figure 30.4-2. Structure of I2C Command Registers
```

| cmd0 | 31       | 30:14    | 13:11   | 10     | 9      | 8          | 7:0        |
|------|----------|----------|---------|--------|--------|------------|------------|
| CMD_DONE | reserved | op_code  | ack_value | ack_exp | ack_check_en | byte_num |

| cmd7 | 31       | 30:14    | 13:11   | 10     | 9      | 8          | 7:0        |
|------|----------|----------|---------|--------|--------|------------|------------|
| CMD_DONE | reserved | op_code  | ack_value | ack_exp | ack_check_en | byte_num |

Command registers, whose structure is illustrated in Figure 30.4-2, are active only when the I2C controller works in master mode. Fields of command registers are:

1. **CMD_DONE**: Indicates that a command has been executed. After each command has been executed, the CMD_DONE bit in the corresponding command register is set to 1 by hardware. By reading this bit, software can tell if the command has been executed. When writing new commands, this bit must be cleared by software.

2. **op_code**: Indicates the command. The I2C controller supports five commands:
    - WRITE: op_code = 1. The I2C controller sends a slave address, a register address (only in dual address mode), and data to the slave.
    - STOP: op_code = 2. The I2C controller sends a STOP bit defined by the I2C protocol. This code also indicates that the command sequence has been executed, and the CMD_Controller stops reading commands. After restarted by software, the CMD_Controller resumes reading commands from command register 0.
```