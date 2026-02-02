**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Section Title:
- **GoBack**

---

#### Subsection Header:
- **Register Name:** RTCIO_ADC_PAD_REG (0x008C)

---

#### Table Description:

| Bit Number | Bit Value |
|------------|-----------|
| 31         | 0         |
| 30         | 0         |
| ...        | ...       |
| 2          | 0         |
| 1           | 0         |
| 0           | 0         |

---

#### Description:

- **Field Name:** RTCIO_ADC_ADCn_HOLD
  - **Description:** Set to 1 to hold the output value on the pin; 0 is for normal operation.
  - **Access Type:** (R/W)

- **Field Name:** RTCIO_ADC_ADCn_MUX_SEL
  - **Description:** Route pin to the digital IO_MUX; (R/W)
    - **Example Description:** 
      ```
      1: route pin to the RTC block.
      ```

- **Field Name:** RTCIO_ADC_ADCn_FUN SEL
  - **Description:** Select the RTC function for this pin. O: select Function, 3: select Function 1; (R/W)

- **Field Name:** RTCIO_ADC_ADCn_SLP SEL
  - **Description:** Signal selection of pin’s sleep mode.
    - Set this bit to 1 to put the pin to sleep;
    - Access Type: (R/W)

- **Field Name:** RTCIO_ADC_ADCn_SLP IE
  - **Description:** Input enable of the pin in sleep mode. 
    - 1 enabled; O disabled.
    - Access Type: (R/W)

- **Field Name:** RTCIO_ADC_ADCn_FUN IE
  - **Description:** Input enable of the pin.  
    - 1 enabled; O disabled;
    - Access Type: (R/W)

---

**Footer Information:**
- Page Number: 156
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Link:** Submit Documentation Feedback