**Chapter Title:**
Chapter 21 I2C Controller (I2C)

**Section Heading:**
21.4 Register Summary

**Body Text:**
The addresses in this section are relative to the I2C base address provided in Table 3.3-6 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Description
- L2CO (I2C0)
- L2CI (I2C1)
- Acc

**Table Content Summary by Sections:**


#### Configuration registers:
- **I2C_CTR_REG**: Transmission configuration register, Address 0x0004 in I2C0 and R/W access.
- **I2C_TO_REG**: Timeout control register, Address 0x000C in both L2CO and L2CI with read/write (R/W) access.

#### Status registers:
- **I2C_SR_REG**: Describes I2C work status, Address 0x0008 in R/W.
- **I2C_FIFO_CONF_REG**: FIFO configuration register, Address 0x3FF53014 to 0x3FF67018 with read-only (RO) access.

#### Timing registers:
- Various timing control and hold configurations for SCL edge transitions. Addresses range from I2C_SDA_HOLD_REG at address 0x3FF53030 in R/W, down to addresses like I2C_SCL_STOP_SETUP_REG ranging between RO.
  
#### Filter registers:
- **I2C_SCL_FILTER_CFG_REG**: SCL filter configuration register with Address 0x3FF53050 and read/write (R/W) access.

#### Interrupt registers:
- Various interrupt status, clear bits, enable settings. For example: 
  - I2C_INT_RAW_REG for raw interrupt status at address 0x3FF67024 in write-only (WO).
  
#### Command registers:
- **I2C_COMDO_REG**: I2C command register O with Address 0x3FF53058 and R/W access.
- Other similar commands like COMD1 and COMD2 at addresses ranging from RO to W/O.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback