**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Figure Caption:**
Figure 29.3-3. Camera Clock

**Body Text with Formula Explanation:**

The following formula shows the relation between the frequencies of CAM_CLK (f_CAM_CLK) and the divider clock source (f_CAM_CLK_s):

\[ f_{\text{CAM_CLK}} = \frac{f_{\text{CAM_CLK_s}}}{N + \frac{b_a}{a}} \]

where:
- \( N \) is an integer value between 2 and 256.
- The value of \( N \) corresponds to the value of LCD_CAM_CAM_CLKM_DIV_NUM in register LCD_CAM_CAM_CTRL_REG as follows:

**Table:**
| Condition | Value |
|-----------|-------|
| When LCD_CAM_CAM_CLKM_DIV_NUM = 0, N = 256. | - |
| When LCD_CAM_CAM_CLKM_DIV_NUM = 1, N = 2. | - |
| When LCD_CAM_CAM_DIV_NUM has any other value, \( N \) = LCD_CAM_CAM_CLKM_DIV_NUM. "b" corresponds to the value of LCD_CAM_CAM_CLKM_DIV_B and "a" to the value of LCD_CAM_CAM_DIV_A. For integer divider, LCD_CAM_CAM_CLKM_DIV_A and LCD_CAM_CAM_CLKM_DIV_B are cleared. For fractional divider, the value of LCD_CAM_CAM_CLKM_DIV_B should be less than the value of LCD_CAM_CAM_CLKM_DIV_A. | - |

**Subtitle:**
29.3.4 LCD_CAM Reset

**Body Text with List Explanation:**

The units in LCD_CAM module can be reset by the following bits:

- **LCD_CAM_LCD_RESET:** set this bit to reset LCD control unit (LCD_Ctrl) and LCD video data format converter (RGB/YCbCr Converter).
- **LCD_CAM_CAM_RESET:** set this bit to reset camera control unit (Camera_Ctrl) and camera video data format converter (RGB/YCbCr Converter).
- **LCD_CAM_LCD_AFIFO_RESET:** set this bit to reset Async Tx FIFO.
- **LCD_CAM_CAM_AFIFO_RESET:** set this bit to reset Async Rx FIFO.

**Notes:**

The above-mentioned reset bits are hardware self-clearing, i.e., the hardware automatically clears these bits once 1 is written. LCD/camera module clock must be configured first before the module and FIFO are reset.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)