**Title:**
Register 15.52, PMS_CORE_0_PIF_PMS CONSTRAIN_10_REG (0x014C)

**Diagram Description:**
- The diagram shows a bit map layout for the register.
- Bits are labeled from top to bottom as follows:
  - Bit 31 is marked as "reserved".
  - Other bits range sequentially down, with some being set in specific positions.

**Bit Labels and Values (from left to right):**
- PMS_CORE_0_PIF_PMS CONSTRAIN_RTCFAST_WORLD_1_H
- PMS CORE_0 PIF PMS CONSTRAIN_RTCFAST_WORLD_1_L
- PMS CORE_0 PIF PMS CONSTRAIN_RTCFAST_WORLD_0_H
- PMS CORE_0 PIF PMS CONSTRAIN_RTCFAST_WORLD_0_L

**Bit Values:**
- The bits are set as follows:
  - Bit positions from top to bottom show "0" for most of the register, except specific bit locations which have a value.

**Text Descriptions (below diagram):**

1. **PMS_CORE_0_PIF_PMS CONSTRAIN_RTCFAST_WORLD_0_L**
   - Configures the permission of CPU0 from Non-secure World to the lower region of RTC Fast Memory.
   - Access: Read/Write

2. **PMS CORE_0 PIF PMS CONSTRAIN_RTCFAST_WORLD_0_H**
   - Configures the permission of CPU0 from Non-secure World to the higher region of RTC Fast Memory.
   - Access: Read/Write

3. **PMS CORE_0_PIF_PMS CONSTRAIN_RTCFAST_WORLD_1_L**
   - Configures the permission of CPU0 from Secure World to the lower region of RTC Fast Memory.
   - Access: Read/Write

4. **PMS CORE_0 PIF PMS CONSTRAIN_RTCFAST_WORLD_1_H**
   - Configures the permission of CPU0 from Secure World to the higher region of RTC Fast Memory.
   - Access: Read/Write

**Footer Information (left side):**
- ESP32-S3 TRM
- Version 1.7