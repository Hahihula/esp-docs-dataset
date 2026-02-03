**Chapter Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Section Header:**
Register 38.1, PCNT_Un_CONF0_REG (n: 0-3) (0x000+0xC*n)

**Continuation Note:**
Continued from the previous page...

**Subsection Title and Description:**
PCNT_CHO_LCTRL_MODE_Un
This register configures how the CHn_POS_MODE/CHn_NEG_MODE settings will be modified when the control signal is low.

- **List Item 1:** 
0: No modification; 1: Invert behavior (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification (R/W)

**Subsection Title and Description:**
PCNT_CH1_NEG_MODE_Un
This register sets the behavior when the signal input of channel 1 detects a negative edge.

- **List Item 1:** 
1: Increment the counter; 2: Decrement the counter; O, 3: No effect on counter (R/W)

**Subsection Title and Description:**
PCNT_CH1_POS_MODE_Uo
This register sets the behavior when the signal input of channel 1 detects a positive edge.

- **List Item 1:** 
1: Increment the counter; 2: Decrement the counter; O, 3: No effect on counter (R/W)

**Subsection Title and Description:**
PCNT_CH1_HCTRL_MODE_Un
This register configures how the CHn_POS_MODE/CHn_NEG MODE settings will be modified when the control signal is high.

- **List Item 1:** 
0: No modification; 1: Invert behavior (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification (R/W)

**Subsection Title and Description:**
PCNT_CH1_LCTRL_MODE_Un
This register configures how the CHn_POS_MODE/CHn_NEG MODE settings will be modified when the control signal is low.

- **List Item 1:** 
0: No modification; 1: Invert behavior (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification (R/W)

**Section Header:**
Register 38.2, PCNT_Un_CONF1_REG (n: 0-3) (0x0004+0xC*n)

**Table Description with Labels and Values:**
- **Column Headers:** 
PCNT_CNT_THRES0_Uo
PCNT_CNT_THRES1_Uo

- **Row Data for Column PCNT_CNT_THRES0_Uo:**
  - Value at Row Position (3): 0x00
  - Reset Value in the last column is indicated as "Reset"

**Footer Information:** 
Espressif Systems  
Page Number and Document Version:
1448 ESP32-S3 TRM (Version 1.7)

**Action Links:**
Submit Documentation Feedback