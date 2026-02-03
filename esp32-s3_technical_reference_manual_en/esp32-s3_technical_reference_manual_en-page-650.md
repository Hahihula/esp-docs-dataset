**Title:**
Chapter 11 System Timer (SYSTIMER)

**Subtitles and Sections:**

- **Register 11.26. SYSTIMER_INT_ENA_REG (0x0064)**
  - Description:
    ```
    31   reserved
    3     SYSTIMER_TARGET2_INT_ENA
    2     SYSTIMER_TARGET1_INT_ENA
    1     SYSTIMER_TARGET0_INT_ENA
    0     Reset

    SYSTIMER_TARGETTO_INT_ENA SYSTIMER_TARGETO_INT enable bit. (R/W)
    SYSTIMER_TARGET1_INT_ENA SYSTIMER_TARGET1 enable bit. (R/W)
    SYSTIMER_TARGET2_INT_ENA SYSTIMER_TARGET2_INT enable bit. (R/W)
    ```

- **Register 11.27. SYSTIMER_INT_RAW_REG (0x0068)**
  - Description:
    ```
    31   reserved
    3     SYSTIMER_TARGET2_INT_RAW
    2     SYSTIMER_TARGET1_INT_RAW
    1     SYSTIMER_TARGET0_INT_RAW
    0     Reset

    SYSTIMER_TARGETTO_INT_RAW SYSTIMER_TARGETO_INT raw bit. (R/WTC/SS)
    SYSTIMER_TARGET1_INT_RAW SYSTIMER_TARGET1 raw bit. (R/WTC/SS)
    SYSTIMER_TARGET2_INT_RAW SYSTIMER_TARGET2_INT raw bit. (R/WTC/SS)
    ```

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
- GoBack

**Additional Information:**
- Submit Documentation Feedback