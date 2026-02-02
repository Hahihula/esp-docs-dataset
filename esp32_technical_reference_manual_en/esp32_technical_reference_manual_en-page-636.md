**Chapter 28: LED PWM Controller (LEDC)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **LEDC_HSCH5_HPOINT_REG** | High-level comparator value configuration register for high-speed channel 5 | 0x3FF59068 | R/W |
| **LEDC_HSCH6_HPOINT_REG** | High-level comparator value configuration register for high-speed channel 6 | 0x3FF5907C | R/W |
| **LEDC_HSCH7_HPOINT_REG** | High-level comparator value configuration register for high-speed channel 7 | 0x3FF59090 | R/W |
| **LEDC_LSCHO_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 0 | 0x3FF590A4 | R/W |
| **LEDC_LSCH1_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 1 | 0x3FF590B8 | R/W |
| **LEDC_LSCH2_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 2 | 0x3FF590CC | R/W |
| **LEDC_LSCH3_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 3 | 0x3FF590E0 | R/W |
| **LEDC_LSCH4_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 4 | 0x3FF590F4 | R/W |
| **LEDC_LSCH5_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 5 | 0x3FF59108 | R/W |
| **LEDC_LSCH6_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 6 | 0x3FF5911C | R/W |
| **LEDC_LSCH7_HPOINT_REG** | High-level comparator value configuration register for low-speed channel 7 | 0x3FF59130 | R/W |

---

### Timer registers

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **LEDC_HSTIMER0_CONF_REG** | High-speed timer 0 configuration | 0x3FF59140 | R/W |
| **LEDC_HSIMER1_CONF_REG** | High-speed timer 1 configuration | 0x3FF59148 | R/W |
| **LEDC_HSIMER2_CONF_REG** | High-speed timer 2 configuration | 0x3FF59150 | R/W |
| **LEDC_HSIMER3_CONF_REG** | High-speed timer 3 configuration | 0x3FF59158 | R/W |
| **LEDC_HSIMER0_VALUE_REG** | High-speed timer 0 current counter value | 0x3FF59144 | RO |
| **LEDC_HSIMER1_VALUE_REG** | High-speed timer 1 current counter value | 0x3FF5914C | RO |
| **LEDC_HSIMER2_VALUE_REG** | High-speed timer 2 current counter value | 0x3FF59154 | RO |
| **LEDC_HSIMER3_VALUE_REG** | High-speed timer 3 current counter value | 0x3FF5915C | RO |
| **LEDC_LSIMER0_CONF_REG** | Low-speed timer 0 configuration | 0x3FF59160 | R/W |
| **LEDC_LSIMER1_CONF_REG** | Low-speed timer 1 configuration | 0x3FF59168 | R/W |
| **LEDC_LSIMER2_CONF_REG** | Low-speed timer 2 configuration | 0x3FF59170 | R/W |
| **LEDC_LSIMER3_CONF_REG** | Low-speed timer 3 configuration | 0x3FF59178 | R/W |
| **LEDC_LSIMER0_VALUE_REG** | Low-speed timer 0 current counter value | 0x3FF59164 | RO |
| **LEDC_LSIMER1_VALUE_REG** | Low-speed timer 1 current counter value | 0x3FF5916C | RO |
| **LEDC_LSIMER2_VALUE_REG** | Low-speed timer 2 current counter value | 0x3FF59174 | RO |
| **LEDC_LSIMER3_VALUE_REG** | Low-speed timer 3 current counter value | 0x3FF5917C | RO |

---

### Interrupt registers

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **LEDC_INT_RAW_REG** | Raw interrupt status | 0x3FF59180 | RO |
| **LEDC_INT_ST_REG** | Masked interrupt status | 0x3FF59184 | RO |
| **LEDC_INT_ENA_REG** | Interrupt enable bits | 0x3FF59188 | R/W |
| **LEDC_INT_CLR_REG** | Interrupt clear bits | 0x3FF5918C | WO |

---

*Espressif Systems*

*ESP32 TRM (Version 5.6)*

*Submit Documentation Feedback*