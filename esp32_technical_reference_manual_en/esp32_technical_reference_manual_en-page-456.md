**Title: Chapter 23 Pulse Count Controller (PCNT)**

**Register Table**
- **Columns**: PCNT_CH1_LCTRL_MODE_Un, PCNT_CH1_HCTRL_MODE_Un, PCNT_CH1_POS_MODE_Un, PCNT_CH1_NEG_MODE_Un, PCNT_CHO_LCTRL_MODE_Un, PCNT_CHO_HCTRL_MODE_Un, PCNT_CHO_POS_MODE_Un, PCNT_CHO_NEG_MODE_Un, PCNT_THRThres1_EN_Un
- **Rows**: 0x0 to 0x9

**Text Descriptions:**

- `PCNT_CH1_LCTRL_MODE_Un`: This register configures how the CH1_POS_MODE/CH1_NEG_MODE settings will be modified when the control signal is low. (R/W) O: No modification; 1: Invert behaviour (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification.

- `PCNT_CH1_HCTRL_MODE_Un`: This register configures how the CH1_POS_MODE/CH1_NEG_MODE settings will be modified when the control signal is high. (R/W) O: No modification; 1: Invert behaviour (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification.

- `PCNT_CH1_POS_MODE_Un`: This register sets the behavior when the signal input of channel 1 detects a positive edge. (R/W) 1: Increment the counter; 2: Decrement the counter; O, 3: No effect on counter

- `PCNT_CH1_NEG_MODE_Un`: This register sets the behaviour when the signal input of channel 1 detects a negative edge. (R/W) 1: Increment the counter; 2: Decrement the counter; O, 3: No effect on counter

- `PCNT_CHO_LCTRL_MODE_Un`: This register configures how the CHO_POS_MODE/CHO_NEG_MODE settings will be modified when the control signal is low. (R/W) O: No modification; 1: Invert behaviour (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification

- `PCNT_CHO_HCTRL_MODE_Un`: This register configures how the CHO_POS_MODE/CHO_NEG_MODE settings will be modified when the control signal is high. (R/W) O: No modification; 1: Invert behaviour (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification

- `PCNT_CHO_POS_MODE_Un`: This register sets the behavior when the signal input of channel 0 detects a positive edge. (R/W) 1: Increase the counter; 2: Decrease the counter; O, 3: No effect on counter

- `PCNT_CHO_NEG_MODE_Un`: This register sets the behaviour when the signal input of channel 0 detects a negative edge. (R/W) 1: Increase the counter; 2: Decrease the counter; O, 3: No effect on counter

- `PCNT_THRThres1_EN_Un`: This is the enable bit for unit n’s thres1 comparator. (R/W)

**Footer**: Continued on the next page...

**Company Information**: Espressif Systems  
**Document Version**: ESP32 TRM (Version 5.6)  
**Page Number**: 456

**Navigation Links**: Submit Documentation Feedback, GoBack