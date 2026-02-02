**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

### Register Section:

#### **Register Name**: SENS_SAR_MEAS_START1_REG (0x0054)

- **Field Descriptions with Binary Representation**:
  - `SENS_SAR_EN_PAD FORCE`: 
    - Description: SAR ADC1 pad enable bitmap is controlled by SW, O: SAR ADC1 pad enable bitmap is controlled by ULP coprocessor. (R/W)
    - Bit Positions and Values: 30-24
  - `SENS_SAR1_EN_PAD`:
    - Description: SARB ADC1 pad enable bitmap; active only when eg_sar1_en_pad_force = 1.
    - Access Type: Read/Write

#### **Field Descriptions**:

- `SENS_MEAS1_START_FORC`:
  - Description: SAR ADC1 controller (in RTC) is started by SW, O: SAR ADC1 controller is started by ULP coprocessor. (R/W)
  
- `SENS_MEAS1_START_SAR`:
  - Description: SAR ADC1 controller (in RTC) starts conversion; active only when reg_meas1_start_force = 1.
  
- `SENS_MEAS1_DONE_SAR`:
  - Description: SAR ADC1 conversion-done indication. (RO)
  
- `SENS_MEAS1_DATA_SAR`:
  - Description: SAR ADC1 data.

---

#### **Register Name**: SENS_SAR_TOUCH_CTRL1_REG (0x0058)

- **Field Descriptions with Binary Representation**:

- `SENS TOUCH OUT_1EN`:
  - Description: wakeup interrupt is generated if SET1 is touched, O: wakeup interrupt is generated only if both SET1 & SET2 are touched.
  
- `SENS TOUCH OUT_SEL`:
  - Description: the touch pad is considered touched when the value of the counter is greater than the threshold; O: the touch pad is considered touched when the value of the counter is less than the threshold.

- `SENS TOUCH XPD WAIT`:
  - Description: The waiting time (in 8 MHz cycles) between TOUCH_START and TOUCH_XPD.
  
- `SENS TOUCH MEAS_DELAY`:
  - Description: The measurement’s duration (in 8 MHz cycles).

---

**Footer Information**: 
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:** 752