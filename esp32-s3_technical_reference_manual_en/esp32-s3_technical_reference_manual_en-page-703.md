**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Section Heading:**
15.7 Protection of CPU VECBASE Registers

**Body Text:**
CPU’s VECBASE registers store the base addresses of interrupts and exceptions table. To protect these registers from unauthorized modification, ESP32-S3 has implemented a special mechanism.

Users can first configure values stored in VECBASE registers to the PMS_CORE_m_VECBASE OVERRIDE_WORLDn_VALUE field of the

PMS_CORE_m_VECBASE OVERRIDE_n_REG register, and then use the configured 

PMS_CORE_m_VECBASE OVERRIDE_WOLDN_VALUE values, instead of VECBASE values. Then by only allowing modification to the PMS_CORE_m_VECBASE OVERRIDE_n_reg register values from the Secure World, the integrity of values stored in VECBASE registers are protected.

**Detailed Steps:**
1. Write the CPU’s VECBASE value in Secure World to the 

PMS_CORE_m_VECBASE OVERRIDE_WORLD0_VALUE field.
2. Write the CPU’s VECBASE value in Non-secure World to the

PMS_CORE_m_VECBASE OVERRIDE_WOLD1_VALUE field.
3. Configure the PMS_CORE_m_VECBASE OVERRIDE_SEL field of the

PMS_CORE_m_VECBASE OVERRIDE_1_REG register by setting it to:

   - 2'b00: just use CPU’s VECBASE register directly.

   - 2'b11: use the value configured in 

PMS_CORE_m_VECBASE OVERRIDE_WOLDN_VALUE, instead of the value in CPU’s VECBASE register

Do not configuring this field to other values.
4. Configure the PMS_CORE_m_VECBASE WORLD_MASK field of the

PMS CORE m_VECBASE OVERRIDE_0_REG register by setting it to:

   - 1: CPU uses WORLD0_VALUE in both the Secure World and the Non-secure World.

   - 0: CPU uses WORLD0_VALUE in the Secure World, and WORLD1_VALUE in the Non-secure World.

**Subsection Heading:**
15.8 Register Locks

**Body Text:**
All ESP32-S3’s permission control related registers can be locked by respective lock registers. When the lock registers are configured to 1, these registers themselves and their related permission control registers are all protected from modification until the next CPU reset.

Note that there isn’t one-to-one correspondence between the lock registers and permission control registers.
See details in Table 15.8-1

**Table Title:**
Table 15.8-1. Lock Registers and Related Permission Control Registers

| Lock Registers | Related Permission Control Registers |
|----------------|---------------------------------------|
| VECBASE Configuration | PMS CORE m_VECBASE OVERRIDE_LOCK_REG |
|                       | PMS CORE m_VECBASE OVERRIDE_0_REG    |
|                       | PMS CORE m_VECBASE OVERRIDE_1_REG     |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)