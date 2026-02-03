**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**GoBack Link:** GoBack

**Note Section:**
- If only one byte is received each time, CAM_Data_in[7:0] is valid data. For such case, users must connect CAM_Data_in[7:0] with the master.

**Section Title: 29.3.6 YUV-RGB Data Format Conversion**

**Body Text:**
The LCD_CAM module supports data format conversion among YUV and RGB. LCD module and camera module each has a data format converter. The converter supports format conversion over:
- BT601 and BT709 standards
- RGB565 (full/limited range) and YUV422/420/411 (full/limited range) formats
- YUV422/420/411 (full/limited range) formats

**Subsection Title: 29.3.6.1 YUV Timing**

**Body Text:**
In LCD_CAM module, assume that there are 8 pixels to be transmitted, corresponding to YUV data [Y_i, U_i, V_i] (i = 1 ~ 8). Then:
- in YUV422 mode, the LCD sends (or the camera receives) the data as follows:

**Diagram:**
\[ Y_1 \quad U_1 \quad Y_2 \quad V_2 \quad Y_3 \quad U_3 \quad Y_4 \quad V_4 \quad Y_5 \quad U_5 \quad Y_6 \quad V_6 \quad Y_7 \quad U_7 \quad Y_8 \quad V_8 \]

- in YUV420 mode, the LCD sends (or the camera receives) the data as follows:

**Diagram:**
\[ Y_1 \quad U_i \quad Y_2 \quad V_i \quad Y_3 \quad U_i \quad Y_4 \quad V_i \quad Y_5 \quad U_i \quad Y_6 \quad V_i \quad Y_7 \quad U_i \quad Y_8 \]

- in YUV411 mode, the LCD sends (or the camera receives) the data as follows:

**Diagram:**
\[ Y_1 \quad U_1 \quad Y_2 \quad V_1 \quad Y_3 \quad U_2 \quad Y_4 \quad V_2 \quad Y_5 \quad U_3 \quad Y_6 \quad V_3 \quad Y_7 \quad U_4 \quad Y_8 \]

**Subsection Title: 29.3.6.2 Data Conversion Configuration**

**Body Text:**
The configuration for format converter in camera module is identical to that in LCD module. Therefore, the configuration process is illustrated below using the format conversion in LCD module as an example:
- Enable YUV-RGB format converter by setting `LCD_CAM_LCD_CONV_BYPASS`.
- Configure the data transfer mode by configuring `LCD_CAM_LCD_CONV_MODE_8BITS_ON`:
  - 0: use 16-bit data transfer mode
  - 1: use 8-bit data transfer mode

**Select the standard by configuring `LCD_CAM_LCD_CONV_PROTOCOL_MODE`:**
- 0: use BT601 standard
- 1: use BT709 standard

**Footer Information:** 
Espressif Systems  
Page Number: 1085  
Document Version: ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback