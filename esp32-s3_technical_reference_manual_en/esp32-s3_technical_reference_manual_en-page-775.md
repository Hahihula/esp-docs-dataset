**Title:**
Register 15.66, PMS_CORE_O_VECBASE OVERRIDE_1_REG (0x1C0)

**Diagram Description:**
- The diagram shows a bit map for the register.
- Bits are labeled from right to left as follows:
  - Bit 31 is not specified in detail but has an associated label "PMS CORE O VECBASE OVERRIDE WORLD VALUE".
  - Other bits (24, 23 through 0) have labels indicating their association with PMS CORE O VECBASE OVERRIDE WORLD VALUE.
- The diagram includes a reset bit at the end.

**Text:**
1. **Register Description:** 
   "PMS_CORE_O_VECBASE OVERRIDE_WORLD_VALUE Configures the VECBASE value for the Secure World (R/W)"

2. **Field Description 1:**
   - Labelled as PMS CORE O VECBASE OVERRIDE WORLD_VALUE
   - Description states it is used to configure VECBASE override.

3. **Field Description 2:** 
   "PMS CORE O VECBASE OVERRIDE SEL Configures VECBASE override."
   - Set to '0' selects VECBASE.
   - Set to '11' selects PMS CORE O VECBASE OVERRIDE_WORLDn_VALUE (R/W)

**Footer:**
- ESP32-S3 TRM (Version 1.7)