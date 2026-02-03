**Title: CPU1 Interrupt Register Summary**

---

### Table of Contents

- **Interrupt Configuration Registers**
  - `INTERRUPT_CORE0_PIF_PMS_MONITOR_VIOLATE`
    - Description: core1_PIF_pms_monitor_violate_interrupt configuration register
    - Address: 0x016C
    - Access: R/W
  - `INTR_MAP_REG`
    - Description: core1_PIF_pms_monitor_violate_size interrupt configuration register
    - Address: 0x0170
    - Access: R/W

- **Interrupt Configuration Registers**
  - `INTERRUPT_CORE0_CACHE_CORE0_ACS_INT_MAP_REG`
    - Description: CACHE CORE0 ACS interrupt configuration register
    - Address: 0x0174
    - Access: R/W
  - `SIZE_INTR_MAP_REG`
    - Description: BACKUP PMS_MONITOR_VIOLATE interrupt configuration register
    - Address: 0x0180
    - Access: R/W

- **Interrupt Configuration Registers**
  - `INTERRUPT_CORE0_CACHE_CORE1_ACS_INT_MAP_REG`
    - Description: CACHE CORE1 ACS interrupt configuration register
    - Address: 0x0184
    - Access: R/W
  - `USB_DEVICE_INT_MAP_REG`
    - Description: USB DEVICE interrupt configuration register
    - Address: 0x018C
    - Access: RO

- **Interrupt Configuration Registers**
  - `INTERRUPT_COREO_PERI_BACKUP_INT_MAP_REG`
    - Description: PERI BACKUP interrupt configuration register
    - Address: 0x0190
    - Access: R/W
  - `DMA_EXTMEM_REJECT_INT_MAP_REG`
    - Description: DMA EXTMEM REJECT interrupt configuration register
    - Address: 0x0194
    - Access: RO

- **Status Registers**
  - `INTERRUPT_COREO_INTR_STATUS_0_REG`
    - Description: Interrupt status register
    - Address: 0x0198
    - Access: R/W
  - `INTERRUPT_COREO_INTR_STATUS_1_REG`
    - Description: Interrupt status register
    - Address: 0x019C
    - Access: RO

- **Status Registers**
  - `INTERRUPT_COREO_INTR_STATUS_2_REG`
    - Description: Interrupt status register
    - Address: 0x01A0
    - Access: R/W
  - `INTERRUPT_COREO_INTR_STATUS_3_REG`
    - Description: Interrupt status register
    - Address: 0x01B0
    - Access: RO

- **Clock Register**
  - `INTERRUPT_COREO_CLOCK_GATE_REG`
    - Description: Clock gate register
    - Address: 0x0200
    - Access: R/W

- **Version Register**
  - `INTERRUPT_COREO_DATE_REG`
    - Description: Version control register
    - Address: 0x021C
    - Access: RO

---

### Configuration Registers Section (9.4.2)

**Configuration Registers**

- `INTERRUPT_CORE1_MAC_INTR_MAP_REG`
  - Description: MAC interrupt configuration register
  - Address: 0x800
  - Access: R/W
  
- `INTERRUPT_CORE1_MAC_NMI_MAP_REG`
  - Description: MAC NMI interrupt configuration register
  - Address: 0x804
  - Access: R/W

- `INTERRUPT_CORE1_PWR_INTR_MAP_REG`
  - Description: PWR interrupt configuration register
  - Address: 0x808
  - Access: R/W