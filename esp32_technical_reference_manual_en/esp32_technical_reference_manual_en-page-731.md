**Title: Chapter 30 Remote Control Peripheral (RMT)**

**Menu/Table of Contents**
- RMT_CH2_TX_LIM_REG | Channel 2 Tx event configuration register | 0x3FF560D8 | R/W
- RMT_CH3_TX_LIM_REG | Channel 3 Tx event configuration register | 0x3FF560DC | R/W
- RMT_CH4_TX_LIM_REG | Channel 4 Tx event configuration register | 0x3FF560E0 | R/W
- RMT_CH5_TX_LIM_REG | Channel 5 Tx event configuration register | 0x3FF560E4 | R/W
- RMT_CH6_TX_LIM_REG | Channel 6 Tx event configuration register | 0x3FF560E8 | R/W
- RMT_CH7_TX_LIM_REG | Channel 7 Tx event configuration register | 0x3FF560EC | R/W

**Other registers**
- RMT_APB_CONF_REG | RMT-wide configuration register | 0x3FF560FO | R/W

**Section Title: 30.4 Registers**

**Body Text:**
The addresses in this section are relative to the RMT base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section **30.3 Register Summary**.

For how to program reserved fields, please refer to Section Programming Reserved Register Field

**Table:**
| Offset | Name | Description |
|--------|------|-------------|
| (reserved) | RMT_MEM_PD | This bit is used to power down the entire RMT RAM block. (It only exists in RMT_CHCONFO). 1: power down memory; 0: power up memory. (R/W) |
| -24 | RMT_CARRIER_OUT_LV_CHn | This bit is used for configuration when the carrier wave is being transmitted. Transmit on low output level with 0, and transmit on high output level with 1. (R/W) |
| ... | ... | ... |

**Additional Registers:**
- **RMT_MEM_SIZE_CHn**: This register is used to configure the amount of memory blocks allocated to channel n.
- **RMT_IDLE_THRES_CHn**: In receive mode, when no edge is detected on the input signal for longer than REG_IDLE_THRES_CHn channel clock cycles, the receive process is finished. (R/W)
- **RMT_DIV_CNT_CHn**: This register is used to set the divider for the channel clock of channel n.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)