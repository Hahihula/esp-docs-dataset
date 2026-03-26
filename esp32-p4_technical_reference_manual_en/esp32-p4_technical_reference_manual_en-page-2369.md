

```markdown
Chapter 44 I2C Controller (I2C) GoBack


## 44.5 Functional Differences Between LP_I2C and I2C

LP_I2C can be used as a master to communicate with external devices when the main system sleeps. LP_I2C includes all the functions of the ESP32-P4 I2Cmaster, but doesn't include any functions of ESP32-P4 I2Cslave. It does not contain any registers related to the I2Cslave. For detailed register list, see 44.8.2 LP_I2C Register Summary.

The design differences between LP_I2C and I2C master are as follows:

* The size of TX/RX RAM in LP_I2C is 16*8 bit, which means the TX/RX FIFO depth is 16 bytes.
* The clock source of APB_CLK in LP_I2C is CLK_AON_FAST. The clock source for I2C_SCLK is configured via LPPERI_LP_I2C_CLK_SEL. The corresponding bits are:

    - 0: CLK_ROOT_FAST
    - 1: CLK_XTALD2
    - 2: PLL_F8M_CLK

Configuring LPPERI_CK_EN_LP_I2C to 1 enables the clock source of I2C_SCLK. Adjust the timing registers accordingly when the clock frequency changes.

See the programming examples of ESP32-P4 I2Cslave in 44.6 for that of LP_I2C.


## 44.6 Programming Example

This section provides programming examples for typical communication scenarios. ESP32-P4 has two I2C controllers. For the convenience of description, I2C masters and slaves in all subsequent figures are ESP32-P4 I2C controllers. I2C master is referred to as I2Cmaster, and I2C slave is referred to as I2Cslave.

### 44.6.1 I2Cmaster Writes to I2Cslave with a 7-bit Address in One Command Sequence
```