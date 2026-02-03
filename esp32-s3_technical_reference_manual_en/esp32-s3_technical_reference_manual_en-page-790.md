**Title: Register 15.94**

**Subtitle: PMS_CORE_0_DRAMO_PMS_MONITOR_2_REG (0x010C)**

**Diagram Description:** 
- The diagram shows a register layout with various fields labeled.
- Fields include:
  - `PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_LOCK`
  - `PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUSWorld`
  - `PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_INTR`

**Field Descriptions:**
1. **PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_INTR**: Stores the interrupt status of dBUS unauthorized access.
2. **PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_LOCK**: Flags atomic access (1: atomic access; 0: not atomic access).
3. **PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_WORLD**: Stores the world that the CPU was in when the unauthorized access happened.
4. **PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR**: Stores the address that CPU’s dBUS was trying to access.

**Additional Information:**
- Secure World; Ob10: Non-secure World (RO)
- Note on addressing:
  - This is an offset of `0x3c00000` and unit is 16, which means the actual address should be `0x3c00000 + PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR * 16`.

**Footer:**
- "Submit Documentation Feedback" on left side.
- Page number (79) and document version ("Version 1.2") at the bottom.

**Navigation Link:** 
- GoBack link is present in blue text towards right-bottom corner of page.