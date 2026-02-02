**Title:**
Chapter 12 DPort Registers

**Subtitle:**
12.4 Register Summary

**Table Headers:**
- Name
- Description
- Address
- Access

**Content (Table Rows):**

1. **System and memory registers**
   - DPOR PRO_BOOT_REMAP_CTRL_REG
     - Description: remap mode for PRO_CPU
     - Address: 0x3FF00000
     - Access: R/W
   - DPOR APP_BOOT_REMAP_CTRL_REG
     - Description: remap mode for APP_CPU
     - Address: 0x3FF00004
     - Access: R/W

2. **DPOR_CACHE_MUX_MODE_REG**
   - Description: the mode of the two caches sharing the memory
   - Address: 0x3FF0007C
   - Access: R/W

**Reset and clock registers**

- DPOR_CPU_PER_CONF_REG
  - Description: Selects CPU clock
  - Address: 0x3FF0003C
  - Access: R/W

**Interrupt matrix registers**

- DPOR_CPU_INTR_FROM_CPU_0_REG
  - Description: interrupt 0 in both CPUs
  - Address: 0x3FF000DC
  - Access: R/W
- DPOR_CPU_INTR_FROM_CPU_1_REG
  - Description: interrupt 1 in both CPUs
  - Address: 0x3FF000E0
  - Access: R/W

**DPOR_CPU_INTR_FROM_CPU_2_REG**

- DPOR_CPU_INTR_FROM_CPU_2_REG
  - Description: interrupt 2 in both CPUs
  - Address: 0x3FF000E4
  - Access: R/W

**DPOR_PRO_INTR_STATUS_REG_0_REG**
  - Description: PRO_CPU interrupt status 0
  - Address: 0x3FF000EC
  - Access: RO

**DPOR_PRO_INTR_STATUS_REG_1_REG**

- DPOR_PRO_INTR_STATUS_REG_1
  - Description: PRO_CPU interrupt status 1
  - Address: 0x3FF000FO
  - Access: R/W

**DPOR_PRO_INTR_STATUS_REG_2_REG**
  - Description: PRO_CPU interrupt status 2
  - Address: 0x3FF000F4
  - Access: RO

**DPOR_APP_INTR_STATUS_REG_0_REG**

- DPOR_APP_INTR_STATUS_REG_0
  - Description: APP_CPU interrupt status 0
  - Address: 0x3FF000F8
  - Access: R/W

**DPOR_APP_INTR_STATUS_REG_1_REG**
  - Description: APP_CPU interrupt status 1
  - Address: 0x3FF000FC
  - Access: RO

**DPOR_APP_INTR_STATUS_REG_2_REG**

- DPOR_APP_INTR_STATUS_REG_2
  - Description: APP_CPU interrupt status 2
  - Address: 0x3FF00100
  - Access: R/W

**DPOR_MAC_NMI_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00104
  - Access: RO

**DPOR_PRO_BB_INT_MAP_REG**

- DPOR_PRO_BB_INT_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF00108
  - Access: R/W

**DPOR_PRO_BT_MAC_INT_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF0010C
  - Access: RO

**DPOR_PRO_BT_BB_INT_MAP_REG**

- DPOR_PRO_BT_BB_INT_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF00114
  - Access: R/W

**DPOR_PRO_BT_NMI_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00118
  - Access: RO

**DPOR_PRO_RWBT_IRQ_MAP_REG**

- DPOR_PRO_RWBT_IRQ_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF0011C
  - Access: R/W

**DPOR_PRO_RWBLE_IRQ_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00120
  - Access: RO

**DPOR_PRO_RWBT_NMI_MAP_REG**

- DPOR_PRO_RWBT_NMI_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF00124
  - Access: R/W

**DPOR_PRO_RWBLE_NMI_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00128
  - Access: RO

**DPOR_PRO_SLCO_INTR_MAP_REG**

- DPOR_PRO_SLCO_INTR_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF0012C
  - Access: R/W

**DPOR_PRO_SLC1_INTR_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00130
  - Access: RO

**DPOR_PRO_UHCHO_INTR_MAP_REG**

- DPOR_PRO_UHCHO_INTR_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF00134
  - Access: R/W

**DPOR_PRO_UHC11_INTR_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00138
  - Access: RO

**DPOR_PRO_TG_TO_LEVEL_INT_MAP_REG**

- DPOR_PRO_TG_TO_LEVEL_INT_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF0013C
  - Access: R/W

**DPOR_PRO_TG_T1_LEVEL_INT_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00140
  - Access: RO

**DPOR_PRO_TG_WDT_LEVEL_INT_MAP_REG**

- DPOR_PRO_TG_WDT_LEVEL_INT_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF00144
  - Access: R/W

**DPOR_PRO_TG_LACT_LEVEL_INT_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00148
  - Access: RO

**DPOR_PRO_TG1_TO_LEVEL_INT_MAP_REG**

- DPOR_PRO_TG1_TO_LEVEL_INT_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF0014C
  - Access: R/W

**DPOR_PRO_TG1_T1_LEVEL_INT_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00150
  - Access: RO

**DPOR_PRO_TG1_WDT-Level_INT_MAP_REG**

- DPOR_PRO_TG1_WDT-Level_INT_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF00154
  - Access: R/W

**DPOR_PRO_TG1_LACT_LEVEL_INT_MAP_REG**
  - Description: interrupt map
  - Address: 0x3FF00158
  - Access: RO

**DPOR_PRO_GPIO_INTERRUPT_MAP_REG**

- DPOR_PRO_GPIO_INTERRUPT_MAP_REG
  - Description: interrupt map
  - Address: 0x3FF0015C
  - Access: R/W

**Footer Information:**
Espressif Systems  
239  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback