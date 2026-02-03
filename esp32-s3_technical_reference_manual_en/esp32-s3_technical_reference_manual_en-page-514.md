**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header:**
Register 6.36. IO_MUX_n_REG (n: GPI00-GPI021, GPI026-GPIO48) (0x0010+4*n)

**Table Description with Labels in Markdown format for clarity and accessibility:**

- **IO_MUX_MCUOE**
  - **Description:** Output enable of the pin in sleep mode.
  - **Values:**
    - `0`: Output disabled
    - `1`: Output enabled

- **IO_MUX_SLP_SEL**
  - **Description:** Sleep mode selection of this pin. Set to 1 to put the pin in sleep mode.

- **IO_MUX_MCU_WPD**
  - **Description:** Pull-down enable of the pin during sleep mode.
  - **Values:**
    - `0`: Internal pull-down disabled (R/W)
    - `1`: Internal pull-down enabled

- **IO_MUX_MCU_WPU**
  - **Description:** Pull-up enable of the pin during sleep mode.

- **IO_MUX_MCU_IE**
  - **Description:** Input enable of the pin during sleep mode.
  - **Values:**
    - `0`: Input disabled (R/W)
    - `1`: Input enabled

- **IO_MUX_MCU_DRV**
  - **Description:** Configures the drive strength of GPIOn during sleep mode.

**Additional Information in Markdown format for clarity and accessibility:**

- **GPIO17 and GPIO18**
  - `0`: ~5 mA
  - `1`: ~20 mA

- **Other GPIOs**
  - `0`: ~5 mA
  - `1`: ~10 mA (R/W)
  - `2`: ~20 mA 
  - `3`: ~40 mA 

**Additional Registers:**

- **IO_MUXFUN_WPD**
  - Pull-down enable of the pin.
  - Values:
    - `1`: Pull-down enabled
    - `0`: Pull-down disabled

- **IO_MUXFUN_WPU**
  - Pull-up enable of the pin. 
  - Values:
    - `1`: Internal pull-up enabled (R/W)
    - `0`: Internal pull-up disabled

- **IO_MUXFUN_IE**
  - Input enable of the pin.
  - Values:
    - `1`: Input enabled
    - `0`: Input disabled 

**Footer:**
Continued on the next page...

**Document Footer Information in Markdown format for clarity and accessibility:**

- Page Number: 514
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Navigation Links at Bottom of Page:** 
- Submit Documentation Feedback