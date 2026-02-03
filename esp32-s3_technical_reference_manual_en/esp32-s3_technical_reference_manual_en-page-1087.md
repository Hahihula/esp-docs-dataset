**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**GoBack Link:** GoBack

**Main Text:**
main. For more detailed configuration, see the configuration examples below.

**Section Heading:**
29.4.1 Configure LCD (RGB Format) as TX Mode

**Body Text with Steps to Follow for Configuration:**
Follow the steps below to configure LCD (RGB format) as TX mode via software:

1. Configure clock according to Section 29.3.3.
2. Configure signal pins according to Table 29.3-1.
3. Enable corresponding interrupts, see Section 29.5.
4. Enable RGB format by setting LCD_CAM_LCD_RGB_MODE_EN.
5. Configure frame format by the following registers. See the figures below.

**List of Configuration Registers:**
- LCD_CAM_LCD_VT_HEIGHT
- LCD_CAM_LCD_VA_HEIGHT
- LCD_CAM_LCD_HB_FRONT
- LCD_CAM_LCD_HT_WIDTH
- LCD_CAM_LCD_HA_WIDTH
- LCD_CAM_VB_FRONT
- LCD_CAM_LCD_VSYNC_WIDTH

**Figure Caption:**
Figure 29.4-1. LCD Frame Structure

**Diagram Description in Figure (with labels):**
The diagram shows the structure of an LCD frame with a blanking region and active video region.

**Footer Information:**
Espressif Systems
Page number: 1087
Document version information: ESP32-S3 TRM (Version 1.7)
Link to Submit Documentation Feedback