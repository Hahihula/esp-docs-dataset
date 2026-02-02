**Chapter Title:**
Chapter 30 Remote Control Peripheral (RMT)

**Section Header:**
Register 30.7, RMT_CHnCARRIER_DUTY_REG (n : 0-7) (0x00B0+4*n)

**Field Description for Register 30.7:**

1. **RMT_CARRIER_HIGH_CHn**: 
   - This field is used to configure the carrier wave's high-level clock period for channel n.
   - The clock source can be either REF_TICK or APB_CLK (R/W).

2. **RMT_CARRIER_LOW_CHn**:
   - This field is used to configure the carrier wave's low-level clock period for channel n.
   - The clock source can be either REF_TICK or APB_CLK (R/W)

**Section Header:**
Register 30.8, RMT_CHn_TX_LIM_REG (n : 0-7) (0x00D0+4*n)

**Field Description for Register 30.8:**

1. **RMT_TX_LIM_CHn**: 
   - When channel n sends more entries than specified here, it produces a TXTHR_EVENT interrupt.
   - This field is configurable.

**Section Header:**
Register 30.9, RMT_APB_CONF_REG (0x00FO)

**Field Description for Register 30.9:**

1. **RMT_MEM_TX.WRAP_EN**: 
   - This bit enables wraparound mode; when the transmitter of a channel has reached the end of its memory block, it will resume sending at the start of its memory region.
   - This field is configurable.

2. **RMT_MEM_ACCESS_EN**:
   - This bit must be 1 in order to access the RMT memory.
   - This field is configurable

**Footer:**
Espressif Systems
Submit Documentation Feedback
ESP32 TRM (Version 5.6)