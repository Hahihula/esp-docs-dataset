**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Header:**
Register 29.13. LCD_CAM_CAM_RGB_YUV_REG (0x000C)

**Table Description:**
- The table shows the register bits with labels such as "LCD_CAM_CONV BITS INV", "LCD_CAM_BYPASS", etc.
- Bits are numbered from 31 to -1, starting at top left and moving right.

**Body Text:**

- **LCD_CAM_CAM_CONV_8BITS_DATA_INV**
  - Swap every two 8-bit input data. 
  - Values:
    - `0`: Disabled
    - `1`: Enabled

- **LCD_CAM_CAMConv_YUV2YUV_MODE**
  - In YUV-to-YUV mode, the following applies: 
    - `0`: Data is converted to YUV422 format.
    - `1`: Data is converted to YUV411 format. 
    - `2`: Disabled
- To enable YUV-to-YUV mode:
  - LCD_CAM_CAM_CONVTrans_MODE must be set to `1`.

- **LCD_CAM_CAMConv_YUV MODE**
  - In YUV-to-RGB and YUV-to-YUV modes, the following applies: 
    - `0`: Input data is in YUV422 format.
    - `1`: Input data is converted from YUV422 to RGB. 

- **LCD_CAM_CAM_conv_PROTOCOL_MODE**
  - Values:
    - `BT601`: `1`
    - `BT709`: `(R/W)`

- **LCD_CAM_CAMData_OUT_RANGE**
  - Configure color range for output data.
  - `0`: Limited color
  - `1`: Full color

- **LCD_CAM_CAMData_IN_RANGE**
  - Configure color range for input data. 
  - `0`: Limited color
  - `1`: Full color

- **LCD_CAM_CAM_conv_8BITS_ON**
  - Values:
    - `0`: 16-bit mode.
    - `1`: 8-bit.

- **LCD_CAM_CAMConvTrans_MODE**
  - Converted to RGB format. 
  - Converted from YUV422 or YUV411 formats

- **LCD_CAM_CAM_conv_BYPASS**
  - Bypass converter:
    - `0`: Enable
    - `1`: Disable

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)