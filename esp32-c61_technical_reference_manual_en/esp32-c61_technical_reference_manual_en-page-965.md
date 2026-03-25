

```markdown
Figure 27.3-2. I2C Slave Architecture

The I2C controller runs either in master mode or slave mode, which is determined by `I2C_MS_MODE`. Figure 27.3-1 shows the architecture of a master, while Figure 27.3-2 shows that of a slave. The I2C controller has the following main parts:

*   Transmit and receive memory (TX/RX RAM): stores data to be transmitted and data received respectively.
*   Command controller (CMD_Controller): generates RSTART, STOP, WRITE, READ, and END commands
*   SCL clock controller (SCL_FSM): generates the timing sequence conforming to the I2C protocol. Figure 27.3-3 and Table 27.3-1 are the timing diagram and corresponding parameters of the I2C protocol.
*   SDA data controller (SCL_MAIN_FSM): controls the execution of I2C commands and the data sequence of the SDA line. It also controls the ACK_deal module to generate the ACK bit and detect the level of the ACK bit on the SDA line.
*   Serial/parallel data converter (DATA_Shifter): shift data between serial and parallel form
*   Filter for SCL (SCL_Filter): remove noises on SCL input signals
*   Filter for SDA (SDA_Filter): remove noises on SDA input signals
*   ACK bit controller (ack_deal): generate the ACK bit and detect the level of the ACK bit on the SDA line under the control of SCL_MAIN_FSM.

Besides, the I2C controller also has a clock module that generates I2C clocks, and a synchronization module that synchronizes the APB bus and the I2C controller.

The clock module is used to select clock sources, turn on and off clocks, and divide clocks. The synchronization module synchronizes signal transfer between different clock domains.
```