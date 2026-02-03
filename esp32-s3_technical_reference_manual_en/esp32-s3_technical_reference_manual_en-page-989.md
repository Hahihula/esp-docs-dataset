Title: Chapter 27 I2C Controller (I2C)

Body Text:
Take SCL_Filter as an example. When enabled, SCL_Filter samples input signals on the SCL line continuously.
These input signals are valid only if they remain unchanged for consecutive I2C_SCL_FILTER_THRES I2C_SCLK clock cycles. Given that only valid input signals can pass through the filter, SCL_Filter can remove glitches whose pulse width is shorter than I2C_SCL_FILTERThres I2C_SCL clock cycles, while SDA_Filter can remove glitches whose pulse width is shorter than I2C_SDA_FILTERThres I2C_SCL clock cycles.

Subtitle: 27.4.3 SCL Clock Stretching

Body Text:
The I2C controller in slave mode (i.e., slave) can hold the SCL line low in exchange for more time to process data.
This function called clock stretching is enabled by setting the I2C_SLAVE_SCL_STRETCH_EN bit.

The following four events occurs:

1. Address match: The address of the slave matches the address sent by the master via the SDA line, and
the R/W bit is 1.

2. RAM being full: RX RAM of the slave is full.
Note that when the slave receives less than 32 bytes,
it is not necessary to enable clock stretching; 
when the slave receives 32 bytes or more, you may interrupt data transmission to wrapped around RAM via the FIFO threshold, or enable clock stretching for more time to process data. When clock stretching is enabled,

I2C_RX_FULL_ACK_LEVEL must be cleared, otherwise there will be unpredictable consequences.

3. RAM being empty: The slave sending ACKs.
If I2C_SLAVE_BYTE_ACK_CTL_EN is set,
the slave pulls SCL low when sending an ACK bit at this stage;
software validates data and configures
I2C_SLAVEBYTE_ACK_LVL to control the level of the ACK bit.
Note that when RX RAM of the slave 
is full, the level of the ACK bit to be sent

is determined by I2C_RX_FULL_ACK_LEVEL,
instead of I2C_SLAVE_BYTE_ACK_LVL. In this case,

I2C_RX_FULL_ACK_LEVEL should also be cleared
to ensure proper functioning of clock stretching.

After SCL has been stretched low, 
the cause of stretching can be read from the 

bit.
Clock stretching is disabled by setting

bit.


Subtitle: 27.4.4 Generating SCL Pulses in Idle State

Body Text:
Usually when the I2C bus is idle,
the SCL line held high.

The I2C controller in ESP32-S3 can be programmed to generate SCL pulses
in idle state.
This function only works 
when the I2C controller is configured as master. If 

bit is set, hardware will send

SCL pulses,

and then automatically clear this bit.
When software reads 0,
set  
to stop.

Subtitle: 27.4.5 Synchronization

Body Text:
I2C registers are configured in APB_CLK domain;
whereas the I2C controller
is configured in asynchronous 
I2C_SCLK domain, therefore,

before being used by the 

controller, register values should be synchronized.
by first writing configuration registers and then writing 1 to  
Registers that need synchronization

are listed in Table.

Footer:
Espressif Systems
989
Submit Documentation Feedback
ESP32-S3 TRM (Version 1.7)