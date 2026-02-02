**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Section Header (with reference to a figure or diagram):**

- **Register 31.17. SENS_SAR_TOUCH_OUT5_REG (0x0080)**
  - **Diagram:**
    ```
    +-------------+-------------+
    |             |             |
    |   31       |     16      |
    |  0x00000   |     15      |
    |             |     0        |
    |             |             |
    |  0x00000   |             |
    |             |             |
    +-------------+-------------+
    ```
  - **Description:**
    - `SENS_TOUCH_meas_OUT8`: The counter for touch pad 8. (RO)
    - `SENS TOUCH_meas_OUT9`: The counter for touch pad 9. (RO)

**Section Header with another reference to a figure or diagram:** 

- **Register 31.18. SENS_SAR_TOUCH_CTRL2_REG (0x0084)**
  - **Diagram:**
    ```
    +-------------+-------------+
    |             |             |
    |   31       |     16      |
    |  0x00000   |     15      |
    |             |     0        |
    |             |             |
    |  0x00000   |             |
    |             |             |
    +-------------+-------------+
    ```
  - **Description:**
    - `SENS_TOUCH_meas_EN_CLR`: Set to clear reg_touch_meas_en. (WO)
    - `SENS_TOUCH_SLEEP_CYCLES`: Sleep cycles for timer. (R/W)

**Additional Descriptions of Registers and their Functions:** 

- `SENS_TOUCH_START_FOR1`: starts the Touch FSM via software; 0: starts the Touch FSM via timer. (R/W)
- `SENS_TOUCH_START_EN1`: starts the Touch FSM; this is valid when reg_touch_start_force is set.
- `SENS TOUCH_START_ESM_EN1`: TOUCH_START & TOUCH_XPD are controlled by the Touch FSM;
  - **Note:** 0: TOUCH_START & TOUCH_XPD are controlled by registers. (R/W)
- `SENS_TOUCH_meas DONE`: Set to 1 by FSM, indicating that touch measurement is done.
- `SENS_TOUCH_meas_EN`: 10-bit register indicating which pads are touched.

**Footer Information:**
Espressif Systems
756 ESP32 TRM (Version 5.6)

**Feedback Link:** Submit Documentation Feedback