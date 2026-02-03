**Title: Chapter 9 Interrupt Matrix (INTERRUPT)**

---

**Register Information**

- **Register Name:** INTERRUPT_COREO_CLOCK_GATE_REG  
  **Address:** 0x019C  
  **Description:** This register is used to control clock-gating of interrupt matrix. (R/W)

- **Bit Description:**
  - `31` and lower bits are reserved.
  - The bit at position `28` has a value '1' indicating the reset state.

**Register Name:** INTERRUPT_COREO_CLK_EN  
  This register is used to control clock-gating of interrupt matrix. (R/W)

---

**Register Information**

- **Register Name:** INTERRUPT_COREO_DATE_REG  
  **Address:** 0x07FC

- **Bit Description:**
  - `31` and lower bits are reserved.
  - The bit at position `28` has a value '0' indicating the reset state.

---

**Section Title: CPU1 Interrupt Registers**

- **Register Information Table:**
  - Register Name | Address
  - INTERRUPT_CORE1_MAC_INR_MAP_REG (INTERRUPT CORE1 MAC Interrupt Map Register) | 0x0800
  - INTERRUPT_CORE1_MAC_NMI_MAP_REG (INTERRUPT CORE1 MAC Non-maskable Interrupt Map Register) | 0x0804
  - INTERRUPT_CORE1_PWR_INR_MAP_REG (INTERRUPT CORE1 Power Interrupt Map Register) | 0x0808
  - INTERRUPT_CORE1_BB_INT_MAP_REG (INTERRUPT CORE1 Bus Bridge Interrupt Map Register) | 0x080C
  - INTERRUPT_CORE1_BT_MAC_INR_MAP_REG (INTERRUPT CORE1 BT MAC Interrupt Map Register) | 0x0810
  - INTERRUPT_CORE1_BT_BB_INT_MAP_REG (INTERRUPT CORE1 BT Bus Bridge Interrupt Map Register) | 0x0814
  - INTERRUPT_CORE1_BT_BB_NMI_MAP_REG (INTERRUPT CORE1 BT Bus Bridge Non-maskable Interrupt Map Register) | 0x0818
  - INTERRUPT_CORE1_RWBT_IRQ_MAP_REG (INTERRUPT CORE1 RWBT IRQ Map Register) | 0x081C
  - INTERRUPT_CORE1_RWBLE_IRQ_MAP_REG (INTERRUPT CORE1 RWBLE IRQ Map Register) | 0x0820
  - INTERRUPT_CORE1_RWBT_NMI_MAP_REG (INTERRUPT CORE1 RWBT Non-maskable Interrupt Map Register) | 0x0824
  - INTERRUPT_CORE1_RWBLE_NMI_MAP_REG (INTERRUPT CORE1 RWBLE Non-maskable Interrupt Map Register) | 0x0828
  - INTERRUPT CORE1_I2C_MST_INR_MAP_REG (INTERRUPT CORE1 I2C Master Interrupt Map Register) | 0x082C

---

**Footer:**
- **Company:** Espressif Systems  
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Page Number:** 559
- **Feedback Link:** Submit Documentation Feedback