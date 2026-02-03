**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

**Register 6.38. GPIO_SIGMADELTA_CG_REG (0x020)**
- **Description:** Clock enable bit of configuration registers for sigma delta modulation.
- **Access Mode:** R/W
- **Bit Description:**
  - **Field:** `GPIO_SD_CLK_EN`
    - **Length:** 1-bit

---

**Register 6.39. GPIO_SIGMADELTA_MISC_REG (0x0024)**
- **Description:** Clock enable bit of sigma delta modulation.
- **Access Mode:** R/W
- **Bit Description:**
  - **Field:** `GPIO_SPI_SWAP`
    - **Length:** 1-bit

---

**Register 6.40. GPIOSD_SIGMADELTA_VERSION_REG (0x0028)**
- **Description:** Version control register.
- **Access Mode:** R/W
- **Bit Description:**
  - **Field:** `GPIO_SD_DATE`
    - **Length:** 1-bit

---

**6.15.4 RTC IO MUX Registers**

The addresses in this section are relative to (Low-Power Management base address provided in Table 4.3-3 in Chapter 4 System and Memory + 0x0400).

---

**Footer:**
- **Company:** Espressif Systems
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Page Number:** 516

**Links:**
- Submit Documentation Feedback