**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

**Register 6.16. GPIO_STATUS_REG (0x0044)**

- **Description:** 
  - `GPIO_STATUS_INT` is an interrupt status register.
  - Each bit can be either of the two interrupt sources for the two CPUs.

- **Enable Bits:**
  - The enable bits in `GPIO_PINn_INT_ENA`, corresponding to the 13-16 bits in `GPIO_PINn_REG` should be set to 1. (R/W)

---

**Register 6.17. GPIO_STATUS_WITS_REG (0x0048)**

- **Description:**
  - `GPIO_STATUS_INT_WITS` is an interrupt status set register.
  - For every bit that is 1 in the value written here, the corresponding bit in `GPIO_STATUS_INT` will be set.

---

**Register 6.18. GPIO_STATUS_WITC_REG (0x004c)**

- **Description:**
  - `GPIO_STATUS_INT_WITC` is an interrupt status clear register.
  - For every bit that is 1 in the value written here, the corresponding bit in `GPIO_STATUS_INT` will be cleared.

---

**Footer:** 
- Espressif Systems
- ESP32 TRM (Version 5.6)
- Submit Documentation Feedback

--- 

*Note: The image also contains a diagram with binary values and labels indicating reset points for each register, but the specific details of these are not transcribed here.*