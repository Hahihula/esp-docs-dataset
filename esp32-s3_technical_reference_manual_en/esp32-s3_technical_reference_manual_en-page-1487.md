**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Section Header (with back reference):**
Register 39.9. RTC_CNTL_TOUCH_DAC1_REG (0x0150)

**Table Description with Labels, Values, and Reset Information for Each Field in the Register:**

- **Field:** RTC_CNTL TOUCH_PAD14_DAC
  - **Description:** Configure the charge/discharge speed (slope) for touch sensor.
  - **Access Type:** Read/Write
  - **Address Offset:** Not specified

- **Field:** RTC_CNTL_TOUCH_PAD13_DAC
  - **Description:** Configure the charge/discharge speed (slope) for touch sensor.
  - **Access Type:** Read/Write
  - **Address Offset:** Not specified

- **Field:** RTC_CNTL TOUCH_PAD12_DAC
  - **Description:** Configure the charge/discharge speed (slope) for touch sensor.
  - **Access Type:** Read/Write
  - **Address Offset:** Not specified

- **Field:** RTC_CNTL_TOUCH_PAD11_DAC
  - **Description:** Configure the charge/discharge speed (slope) for touch sensor.
  - **Access Type:** Read/Write
  - **Address Offset:** Not specified

- **Field:** RTC_CNTL TOUCH_PAD10_DAC
  - **Description:** Configure the charge/discharge speed (slope) for touch sensor.
  - **Access Type:** Read/Write
  - **Address Offset:** Not specified

**Subsection Title:**
39.7.2 SENSOR (RTC_PERI) Registers

**Body Text with Reference to Table and System Memory Addressing Scheme:**
The addresses in this section are relative to the [Low Power Management base address + 0x800] provided in Table 4.3-3 in Chapter 4 System Memory.

**Register Description for SENS_SAR_READER1_CTRL_REG (0x0000):**

- **Field:** SENS_SAR1_CLK_DIV
  - **Description:** Clock divider.
  - **Access Type:** Read/Write

- **Field:** SENS_SAR1_DATA_INV
  - **Description:** Invert SAR ADC1 data.
  - **Access Type:** Read/Write

- **Field:** SENS_SAR1_INT_EN
  - **Description:** Enable SAR ADC1 to send out interrupt.
  - **Access Type:** Read/Write

**Footer:**
Espressif Systems, Page number (1487), Document version information.