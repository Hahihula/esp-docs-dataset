**Title:**
Chapter 35 LED PWM Controller (LEDC)

**Subtitle:**
35.4 Register Summary

**Body Text:**

The addresses in this section are relative to **LED PWM Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory**.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content (Partial):**

| Configuration Register | Description | Address | Access |
|-------------------------|-------------|--------|-------|
| LEDC_CHO_CONFO_REG     | Configuration register 0 for channel 0 | 0x0000 | varies |
| LEDC_CHO_CONF1_REG     | Configuration register 1 for channel 0 | 0x000C | R/W   |
| ...                     | ...         | ...    | ...   |

**Subsections:**

- **Hpoint Register**
  - LEDC_CHO_HPOINT_REG
  - ...
  
- **Duty Cycle Register**
  - LEDC_CHO_DUTY_REG
  - ...

**Footer Text:**
Espressif Systems

1317 ESP32-S3 TRM (Version 1.7)

Submit Documentation Feedback