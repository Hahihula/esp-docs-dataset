**Title:**
Chapter 15 Permission Control (PMS)

**Register Information:**
- **Name:** Register 15.54, PMS_CORE_0_PIF_PMS CONSTRAINT_12_REG (0x0154)
- **Description:** This register is used to configure the permission of CPU0 from different worlds.

**Bit Description Table:**
| Bit | Description |
|-----|-------------|
| 31 | reserved |
| ... | ... |
| 6 | PMS CORE_0_PIF_PMS CONSTRAINT_RTCSLOW_0_WORLD_1_H |
| 5 | PMS CORE_0_PIF_PMS CONSTRAINT_RTCSLOW_0_WORLD_1_L |
| 4 | PMS CORE_0_PIF_PMS CONSTRAINT_RTCSLOW_0_WORLD_0_H |
| ... | ... |
| 2 | PMS CORE_0_PIF_PMS CONSTRAINT_RTCSLOW_0_WORLD_0_L |
| 1 | reserved |
| 0 | Reset |

**Permissions Configuration:**
- **PMS_CORE_0_PIF_PMS CONSTRAINT_RTCSLOW_0_WORLD_0_L:** Configures the permission of CPU0 from Secure World to the lower region of RTC Slow Memory O. (R/W)
- **PMS CORE_0 PIF PMS CONSTRAINT RTCSLOW 0 WORLD 0 H:** Configures the permission of CPU0 from Secure World to the higher region of RTC Slow Memory O. (R/W)
- **PMS CORE_0 PIF PMS CONSTRAINT RTCSLOW 0 WORLD 1 L:** Configures the permission of CPU0 from Non-secure World to the lower region of RTC Slow Memory O. (R/W)
- **PMS CORE_0 PIF PMS CONSTRAINT RTCSLOW 0 WORLD 1 H:** Configures the permission of CPU0 from Non-secure World to the higher region of RTC Slow Memory O. (R/W)

**Footer:**
- "Submit Documentation Feedback"
- Document version information at bottom left corner.
- Navigation link labeled "GoBack" on right side.

**Side Texts and Labels:**
- Left vertical text reads, "Espressif Systems."
- Right top label says, "Chapter 15 Permission Control (PMS)."

(Note: The detailed bit descriptions are not fully listed here due to the length of information provided in each column.)