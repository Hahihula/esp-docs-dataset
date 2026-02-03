**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section with Code and Explanation:**

- **Text:** To configure the integer divider, clear `I2S_TX/RX_CLKM_DIV_X` and `I2S_TX/RX_CLKM_DIV_Z`, then set `LKM_DIV_Y` to 1.

- **Note Box (Blue Border):**
  - Text inside Note box: Using fractional divider may introduce some clock jitter.
  
**Body Text with Formulae Explanation:** 

The serial clock (`BCK`) of the I2Sn TX/RX unit is divided from `I2Sn_TX/RX_CLK`, as shown in Figure 28.6-1.

In master TX mode, the serial clock BCK for I2Sn TX unit is `I2SnO_BCK_out`, divided from `I2Sn_TX_CLK`. That is:

\[ f_{I2SnO\_BCK\_out} = \frac{f_{I2Sn\_TX\_CLK}}{MO} \]

- **Note:** “MO” is an integer value:
  - Formula: \( MO = I2S_TX_BCK_DIV_NUM + 1 \)

**Additional Note Box (Blue Border):**

In master RX mode, the serial clock BCK for `I2Sn` RX unit is `I2SnRXout`, divided from `I2Sn_RX_CLK`. That is:

\[ f_{I2SnRXout} = \frac{f_{I2Sn_RX_CLK}}{MI} \]

- **Note:** “MI” is an integer value:
  - Formula: \( MI = I2S_RX_BCK_DIV_NUM + 1 \)

**Additional Note Box (Blue Border):**

In slave mode, make sure `f_{I2Sn_TX/RX_CLK} >= 8 * f_{BCK}`. The I2Sn module can output `I2Sn_MCLKout` as the master clock for peripherals.

- **Note:** 
  - \( I2S_RX_BCK_DIV_NUM \) must not be configured as 1.
  - In slave mode, make sure `f_{I2Sn_TX/RX_CLK} >= 8 * f_{BCK}`. The I2Sn module can output `I2Sn_MCLKout` as the master clock for peripherals.

**Subsection Title:**
28.7 I2Sn Reset

The units and FIFOs in an I2Sn module are reset by the following bits:

- **List Items:** 
  - `I2Sn_TX/RX units`: reset by the bits `I2S_TX_RESET` and `I2S_RX_RESET`.
  - `I2Sn TX/RX FIFO`: reset by the bits `I2S_TX_FIFO_RESET` and `I2S_RX_FIFO_RESET`.

**Additional Note Box (Blue Border):**

The I2Sn module clock must be configured first before the module and FIFO are reset.

**Subsection Title:**
28.8 I2Sn Master/Slave Mode

The ESP32-S3 I2Sn module can operate as a master or a slave, depending on the configuration of `I2S_TX_SLAVE_MOD` and `I2S_RX_SLAVE_MOD`.

**Footer Information:** 
- Page number: 1046
- Document version information (bottom right): ESP32-S3 TRM (Version 1.7)
- Navigation Links:
  - Submit Documentation Feedback