Title: Chapter 27 I2C Controller (I2C)

Body Text:
- "I2C_SCL_MAIN_ST_INT interrupt is triggered, and then SCL_MAIN_FSM goes to idle state. The value of I2C_SCL_MAIN_ST_TO_I2C should be less than or equal to 22, which means SCL_MAIN_FSM could remain unchanged for \(2^{22}\) clock cycles at most before the interrupt is generated."

Subtitle: Timeout control
- "Timeout control for SCL is enabled by setting I2C_TIMEOUT_EN. When the level of SCL remains unchanged for more than 2\(^{I2C TIMEOUT VALUE}\) clock cycles, an I2C TIMEOUT_INT interrupt is triggered, and then the I2C bus goes to idle state."

Section Title: Command Configuration
- "When the I2C controller works in master mode, CMD_Controller reads commands from 8 sequential command registers and controls SCL_FSM and SCL_MAIN_FSM accordingly."
- Table:
  - Column Headers: cmd0 (reserved), op_code, ack_value, ack_exp, ack_check_en, byte_num
  - Row Data for cmd0: 31, reserved, 13:11, 10, 9, 8, 7:0

- Table:
  - Column Headers: cmd7 (reserved), op_code, ack_value, ack_exp, ack_check_en, byte_num
  - Row Data for cmd7: 31, reserved, 13:11, 10, 9, 8, 7:0

Caption under the table:
- "Figure 27.4-2. Structure of I2C Command Registers"

Body Text (continued):
- "Command registers, whose structure is illustrated in Figure 27.4-2, are active only when the I2C controller works in master mode. Fields of command registers are:"
  - List:
    1. CMD_DONE: Indicates that a command has been executed. After each command has been executed, the CMD_DONE bit in the corresponding command register is set to 1 by hardware. By reading this bit, software can tell if the command has been executed. When writing new commands, this bit must be cleared by software.
    2. op_code: Indicates the command. The I2C controller supports five commands:
      - RSTART: op_code = 6. The I2C controller sends a START bit or a RSTART bit defined by the I2C protocol.
      - WRITE: op_code = 1. The I2C controller sends a slave address, a register address (only in double addressing mode) and data to the slave.
      - READ: op_code = 3. The I2C controller reads data from the slave.
      - STOP: op_code = 2. The I2C controller sends a STOP bit defined by the I2C protocol. This code also indicates that the command sequence has been executed, and the CMD_Controller stops reading commands. After restarted by software, the CMD_Controller resumes reading commands from command register O.
    3. END: op_code = 4. The I2C controller pulls the SCL line down and suspends I2C communication. This code also indicates that the command sequence has completed, and the CMD_Controller stops executing commands. Once software refreshes data in command registers and the RAM, the CMD_Controller can be restarted to execute commands from command register O again."

Footer:
- "Espressif Systems"
- Page number: 993
- Document version information (partially visible): ESP32-S3 TRM (Version 1.7)
- Link: Submit Documentation Feedback