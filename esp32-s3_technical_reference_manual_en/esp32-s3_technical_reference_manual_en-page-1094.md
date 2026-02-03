**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Link:**
GoBack

**Register Information:**
- **Register Name:** LCD_CAM_LCD_LCD_RGB_YUV_REG (0x010)
- **Description of Register:**
  - **Field Descriptions for Bits in the Register:**
    - `31` to `29`: Reserved
    - `28`: LCD_CAM_LCD_CONV_BYPASS MODE
      - Description:
        - `0`: Data is converted from YUV422 format.
        - `1`: Data conversion must be set up for YUV-to-YUV mode. 3: disabled.

**Fields and Their Functions in the Register:**
- **LCD_CAM_LCD_CONV_8BITS_DATA_INV (R/W)**
  - Description:
    - Swap every two 8-bit input data.
    - `1`: Enabled
    - `0`: Disabled

- **LCD_CAM_LCD_CONV_YUV2YUV_MODE (R/W)**
  - Description:
    - In YUV-to-YUV mode, the register decides whether to convert from one format to another or not. 
    - `0`: Data is converted.
    - `1`: Data conversion must be set up for YUV-to-YUV mode.

- **LCD_CAM_LCD_CONV_YUV_MODE (R/W)**
  - Description:
    - In YUV-to-RGB mode, the register decides whether to convert from one format to another or not. 
    - `0`: Input data is in YUV422 format.
    - `1`: Input data must be converted.

- **LCD_CAM_LCD_CONV_PROTOCOL_MODE (R/W)**
  - Description:
    - In BT601 mode, the register decides whether protocol conversion should occur or not. 
    - `BT601`: Mode
    - `BT709`: Mode

- **LCD_CAM_LCD_CONV_DATA_OUT_MODE (R/W)**
  - Description: Configure color range for output data.
    - `0`: Limited color range.

- **LCD_CAM_LCD_CONV_DATA_IN_MODE (R/W)**
  - Description: Configure color range for input data. 
    - `0`: Limited color range

- **LCD_CAM_LCD_CONV_MODE_8BITS_ON (R/W)**
  - Description:
    - In 16-bit mode, the register decides whether to use an 8-bit conversion.
    - `0`: 8-bit
    - `1`: 16-bit.

- **LCD_CAM_LCD_CONV_RGB_TO_YUV (R/W)**
  - Description: Convert data from RGB format into YUV422 or other formats as specified by the register settings. 

- **LCD_CAM_LCD_CONV_BYPASS (R/W)**
  - Description:
    - Bypass converter.
    - `0`: Enable
    - `1`: Disable

**Footer Information:**
- Page Number: 1094
- Document Version: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems
- Link for Submitting Documentation Feedback