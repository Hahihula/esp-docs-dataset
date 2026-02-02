**Title:**
Chapter 21 I2C Controller (I2C)

**Subtitle:**
21.3.2 Architecture

**Body Text:**
An I2C controller can operate either in master mode or slave mode. The I2C_MS_MODE register is used to select the mode. Figure 21.3-1 shows the I2C Master architecture, while Figure 21.3-2 shows the I2C Slave architecture.

**Figure Captions:**
- **Figure 21.3-1:** I2C Master Architecture
- **Figure 21.3-2:** I2C Slave Architecture

**List of Units in L2C Controller (with descriptions):**
- RAM, which is a sizeable unit with dimensions \(32 \times 8\) bits and directly mapped onto the address space of CPU cores starting at address `REG_I2C_BASE+0x100`. Each byte stored starts from memory locations: first byte at +0x100, second byte at +0x104, third byte at +0x108. Users need to set register I2C_NONFIFO_EN.
- Note that the L2C controller only supports NON-FIFO mode.

**Additional Information about Registers and State Machine:**
- A CMD_Controller with 16 command registers (cmd0 ~ cmd15) used by both Master for control data transmission. One command at a time is executed per I2C controller.
- SCL FSM, which controls the SCL clock using state machine `I2C_SCL_HIGH_PERIOD_REG` and other related components.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32 TRM (Version 5.6)