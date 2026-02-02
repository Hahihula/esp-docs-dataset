**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.16. EMACFF_REG (0x1004)

**Body Text with Subsections and Details:**

Continued from the previous page...

- **DAIF**: When this bit is set, the Address Check block operates in inverse filtering mode for the DA address comparison for both unicast and multicast frames. When reset, normal filtering of frames is performed.
  - (R/W)

- **PMODE**: When this bit is set, the Address Filter module passes all incoming frames irrespective of the destination or source address. The SA or DA Filter Fails status bits of the Receive Status Word are always cleared when PR(PRT_RATIO) is set.

**Register Title:**
Register 24.17. EMACGMIIADDR_REG (0x1010)

**Table Description with Labels and Values for Each Bit Field in Register MIACFF_REG:**

- **MIDEV**: This field indicates which of the 32 possible PHY devices are being accessed.
  - (R/W)
  
- **MIIREG**: This field selects the desired MII register in the selected PHY device.
  - (R/W)

- **MIICSRCLK**: This field selects the APB clock frequency. It has two values:
  - `4'b0000`: The APB clock frequency is 80 MHz, and the MD Clock frequency is APB_CLK/42
  - `4'b0011`: The APB clock frequency is 40 MHz; MDC clock frequency = APB_CLK/26 (R/W)

- **MIWRITE**: When set, this field indicates to the PHY that it's a Write operation using MI_DATA. If not set, it means Read operation placing data in MI_DATA.
  - (R/W)

- **MIIBUSY**: This field is used with MIIREG and MI_DATA for indicating busy status before writing or reading from MI_DATA.

**Additional Notes:**
Before writing to MIIREG and MI_DATA fields should read logic '0' as idle state by default. To set up software (user) access, it's recommended that this field be kept valid until cleared hardware-wise.
- MII_DATA remains unchanged when accessed; data is cleared upon completion.

**Important Note:**
ESP32 MAC does not receive ACK from PHY during read or write to MIREG and MI_DATA fields. This behavior can affect the communication protocol handling in certain scenarios (R/WS/SC).

**Footer Information:**
Espressif Systems
Page 504 of ESP32 TRM (Version 5.6)
Submit Documentation Feedback