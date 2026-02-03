**Title:**
Register 15.93. PMS_CORE_0_IRAMO_PMS_MONITOR_2_REG (0x00EC)

**Body Text and Descriptions of Register Fields:**

- **PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_INR**: Stores the interrupt status of CPU0’s unauthorized IBUS access. (RO)
  
- **PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_WR**: Indicates the access direction.
  - `1`: write
  - `0`: read
  Note: This field is only valid when PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_LOADSTORE is `1`. (RO)

- **PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_LOADSTORE**: Indicates the instruction direction.
  - `1`: load/store
  - `0`: instruction execution. (RO)
  
- **PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_WORLD**: Stores the world the CPU0 was in when the illegal access happened.
  - `0b01`: Secure World; `0b10`: Non-secure World. (RO)

- **PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR**: Stores the address that CPU0’s IBUS was trying to access unauthorizedly.

Note: This is an offset to 0x4000000 and the unit is `4`, which means the actual address should be 0x4000000 + PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR * `4`. (RO)

**Diagram Description:**
The diagram shows a bit map layout for Register 15.93, with labels indicating different fields and their positions within the register.

- **Fields**: 
  - `PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_INR`
  - `PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_WR`
  - `PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_LOADSTORE`
  - `PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS WORLD`
  - `PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR`

- **Bit Positions**:
  - The diagram shows the bit positions for each field, with specific bits highlighted and labeled.

**Footer:**
ESPROS-S3 TRM (Version 1.7)