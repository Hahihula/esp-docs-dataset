

- SCL clock controller (SCL_FSM): generate the timing sequence conforming to the I2C protocol. Figure 30.3-3 and Figure 30.3-1 are the timing diagram and corresponding parameters of the I2C protocol.
- SDA data controller (SDA_MAIN_FSM): control the execution of I2C commands and the data sequence of the SDA line. It also controls the ack_deal module to generate the ACK bit and detect the level of the ACK bit on the SDA line.
- Serial/parallel data converter (DATA_Shifter): shift data between serial and parallel form
- Filter for SCL (SCL_Filter): remove noises on SCL input signals
- Filter for SDA (SDA_Filter): remove noises on SDA input signals
- ACK bit controller (ack_deal): generate the ACK bit and detect the level of the ACK bit on the SDA line under the control of SCL_MAIN_FSM.

Besides, the I2C controller also has a clock module that generates I2C clocks, and a synchronization module that synchronizes the APB bus and the I2C controller.

The clock module is used to select clock sources, turn on and off clocks, and divide clocks. The synchronization module synchronizes signal transfer between different clock domains.

Fig.31 Definition of timing for F/S-mode devices on the I²C-bus.

Figure 30.3-3. I2C Protocol Timing (Cited from Fig.31 in The I2C-bus specification Version 2.1)