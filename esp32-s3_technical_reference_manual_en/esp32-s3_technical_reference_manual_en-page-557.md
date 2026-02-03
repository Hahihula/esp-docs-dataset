**Title: Chapter 9 Interrupt Matrix (INTERRUPT)**

---

**Body Text and Registers List**

- **Register 9.67:** INTERRUPT_COREO_CPU_INTR_FROM_CPU_1_MAP_REG (0x0140)
- **Register 9.68:** INTERRUPT_COREO_CPU_INTR_FROM_CPU_2_MAP_REG (0x0144)
- **Register 9.69:** INTERRUPT_COREO_CPU_INTR_FROM_CPU_3_MAP_REG (0x0148)
- **Register 9.70:** INTERRUPT COREO_DMA_ABPERI_PMS_MONITOR_VIOLATE_INTR_MAP_REG (0x0150)
- **Register 9.71:** INTERRUPT COREO_O_IRAMO_PMS_MONITOR_VIOLATEINTR_MAP_REG (0x0154)
- **Register 9.72:** INTERRUPT COREO_O_DRAMO_PMS_MONITOR_VIOLATEINTR_MAP_REG (0x0158)
- **Register 9.73:** INTERRUPT COREO_O_PIF_PMS_MONITOR_VIOLATEINTR_MAP_REG (0x015C)
- **Register 9.74:** INTERRUPT COREO_O_PIFF_PMS_MONITOR_VIOLATE_SIZE_INTR_MAP_REG (0x0160)
- **Register 9.75:** INTERRUPT COREO_I_IRAMO_PMS_MONITOR_VIOLATEINTR_MAP_REG (0x0164)
- **Register 9.76:** INTERRUPT COREO_I_DRAMO_PMS_MONITOR_VIOLATEINTR_MAP_REG (0x0168)
- **Register 9.77:** INTERRUPT COREO_I_PIFF_PMS_MONITOR_VIOLATEINTR_MAP_REG (0x016C)
- **Register 9.78:** INTERRUPT COREO_I_PIFF_PMS_MONITOR_VIOLATE_SIZE_INTR_MAP_REG (0x0170)
- **Register 9.79:** INTERRUPT COREO_BACKUP_PMS_MONITOR_VIOLATEINTR_MAP_REG (0x0174)
- **Register 9.80:** INTERRUPT COREO_CACHE_COREO_ACS_INT_MAP_REG (0x0178)
- **Register 9.81:** INTERRUPT COREO_CACHE COREA1 ACS_INT_MAP_REG (0x017C)
- **Register 9.82:** INTERRUPT COREO_USB_DEVICE_INT_MAP_REG (0x0180)
- **Register 9.83:** INTERRUPT COREO_PERI_BACKUP_INT_MAP_REG (0x0184)
- **Register 9.84:** INTERRUPT COREO_DMA_EXTMEM_REJECT_INT_MAP_REG (0x0188)

---

**Diagram Description**

The diagram shows a mapping of interrupt sources to CPU external interrupts, with specific registers and their addresses indicated.

**Interrupt Source Mapping Diagram:**
```
INTERRUPT_COREO_SOURCE_Y_MAP
```

- **Description:** Map interrupt signal of Source_Y to one of CPU0 external interrupt. Can be configured as 0 ~ 5, 8 ~ 10, 12 ~ 14, 17 ~ 28, 30 ~ 31.
- **Note:** The remaining values are invalid.

**Interrupt Status Register:**
```
INTERRUPT COREO_INTR_STATUS O_REG
```

- **Description:** This register stores the status of the first 32 interrupt sources. (RO)

---

**Footer**

Espressif Systems  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback

Page Number: [557](#)