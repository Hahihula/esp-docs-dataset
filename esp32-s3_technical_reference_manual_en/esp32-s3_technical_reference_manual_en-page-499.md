**Chapter 6: IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Table of Configuration Registers for GPIOs:
| Name | Description | Address | Access |
|------|-------------|---------|--------|
| IO_MUX_GPIO40_REG | Configuration register for GPIO40 | 0x00A4 | R/W |
| IO_MUX_GPIO41_REG | Configuration register for GPIO41 | 0x00A8 | R/W |
| IO_MUX_GPIO42_REG | Configuration register for GPIO42 | 0x00AC | R/W |
| IO_MUX_GPIO43_REG | Configuration register for GPIO43 | 0x00B0 | R/W |
| IO_MUX_GPIO44_REG | Configuration register for GPIO44 | 0x00B4 | R/W |
| IO_MUX_GPIO45_REG | Configuration register for GPIO45 | 0x00B8 | R/W |
| IO_MUX_GPIO46_REG | Configuration register for GPIO46 | 0x00BC | R/W |
| IO_MUX_GPIO47_REG | Configuration register for GPIO47 | 0x00C0 | R/W |
| IO_MUX_GPIO48_REG | Configuration register for GPIO48 | 0x00C4 | R/W |

---

**6.14.3 SDM Output Register Summary**

The addresses in this section are relative to (GPIO base address provided in Table 4.3-3 in Chapter 4 System and Memory + 0x0F00).

The abbreviations given in Column **Access** are explained in Section [Access Types for Registers](#).

---

### Configuration Registers

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GPIO_SIGMADELTA0_REG | Duty Cycle Configure Register of SDMO | 0x0000 | R/W |
| GPIO_SIGMADELTA1_REG | Duty Cycle Configure Register of SDM1 | 0x0004 | R/W |
| GPIO_SIGMADELTA2_REG | Duty Cycle Configure Register of SDM2 | 0x0008 | R/W |
| GPIO_SIGMADELTA3_REG | Duty Cycle Configure Register of SDM3 | 0x000C | R/W |
| GPIO_SIGMADELTA4_REG | Duty Cycle Configure Register of SDM4 | 0x0010 | R/W |
| GPIO_SIGMADELTA5_REG | Duty Cycle Configure Register of SDM5 | 0x0014 | R/W |
| GPIO_SIGMADELTA6_REG | Duty Cycle Configure Register of SDM6 | 0x0018 | R/W |
| GPIO_SIGMADELTA7_REG | Duty Cycle Configure Register of SDM7 | 0x001C | R/W |
| GPIO_SIGMADELTA_CG_REG | Clock Gating Configure Register | 0x0020 | R/W |
| GPIO_SIGMADELTA_MISC_REG | MISC Register | 0x0024 | R/W |
| GPIO_SIGMADELTA_VERSION_REG | Version Control Register | 0x0028 | R/W |

---

**6.14.4 RTC IO MUX Register Summary**

The addresses in this section are relative to (Low-Power Management base address provided in Table 4.3-3 in Chapter 4 System and Memory + 0x0400).

The abbreviations given in Column **Access** are explained in Section [Access Types for Registers](#).

---

### GPIO configuration/data registers

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RTC_GPIO_OUT_REG | RTC GPIO output register | 0x0000 | R/W |
| RTC_GPIO_OUT_W1TS_REG | RTC GPIO output bit set register | 0x0004 | WO |
| RTC_GPIO_OUT_W1TC_REG | RTC GPIO output bit clear register | 0x0008 | WO |
| RTC_GPIO_ENABLE_REG | RTC GPIO output enable register | 0x000C | R/W |
| RTC_GPIO_ENABLE_WITS_REG | RTC GPIO output enable bit set register | 0x0010 | WO |

---

**Espressif Systems**

499

ESP32-S3 TRM (Version 1.7)

Submit Documentation Feedback