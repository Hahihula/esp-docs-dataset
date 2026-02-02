**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** GoBack

**Register Section Header:**
Register 6.51. RTCIO_XTAL_32K_PAD_REG (0x08C)

**Continuation Note:**
Continued from the previous page...

**Register Description and Details Table:**

- **RTCIO_XTAL_X32P_SLP_OE:** Output enable of the pin in sleep mode.
  - Values:
    - `1`: enabled
    - `0`: disabled

- **RTCIO_XTAL_X32P_FUN_I:** Input enable of the pin. 
  - Values: 
    - `1`: enabled; 
    - `0`: disabled.

- **RTCIO_XTAL_DRES_XTAL_32K:** 32K XTAL resistor bias control.
  - Access Mode (R/W)

- **RTCIO_XTAL_DBIAS_XTAL_32K:** 32K XTAL self-bias reference control. 
  - Access Mode (R/W)

**Register Section Header:**
Register 6.52. RTCIO TOUCH_CFG_REG (0x0900)

**Binary Register Description and Details Table with Bits Indicated for Each Field:**

- **RTGIO_TOUCH_BIAS:** Touch sensor bias power on bit.
  - Values:
    - `1`: powered
    - `0`: disabled

- **RTGIO TOUCH_DREFH:** Touch sensor saw wave top voltage. 
  - Access Mode (R/W)

- **RTGIO TOUCH_DREFL:** Touch sensor saw wave bottom voltage. 
  - Access Mode (R/W)

- **RTGIO_TOUCH_DRANGE:** Touch sensor saw wave voltage range.
  - Values:
    - `1`: enabled
    - `0`: disabled

- **RTGIO_TOUCH_DCUR:** Touch sensor bias current when BIAS_SLEEP is enabled, this setting available. 
  - Access Mode (R/W)

**Footer:**
Espressif Systems  
ESP32 TRM (Version 5.6)  

**Link for Submitting Documentation Feedback:**
Submit Documentation Feedback