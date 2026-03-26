

```markdown
- LCD_CAM_LCD_TRANSDONE_INT: Triggered when the LCD module finishes the transmission.
- LCD_CAM_LCD_VSYNC_INT: Triggered when the LCD module transmits a whole frame.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.

## 38.5 Software Configuration Process

**Note:**
Updating the configurations of the LCD module or the Camera module requires setting the `LCD_CAM_LCD_UPDATE` and `LCD_CAM_CAM_UPDATE` respectively to synchronize registers from the APB clock domain to the LCD/camera clock domain. Check the configuration examples below for more details.

### 38.5.1 Configure LCD (RGB Format) as TX Mode

Follow the steps below to configure LCD (RGB format) as TX mode via software:

1. Configure clock according to Section 38.3.3.
2. Configure signal pins according to Table 38.3-1 and Chapter 9 GPIO Matrix and IO MUX.
3. Enable corresponding interrupts, see Section 38.4.
4. Enable RGB format by setting `LCD_CAM_LCD_RGB_MODE_EN`.
5. Configure frame structure according to Section 38.3.7.1.
6. Set `LCD_CAM_LCD_UPDATE` so that the configurations take effect.
7. Reset TX control unit (`LCD_Ctrl`) and Async TX FIFO as described in Section 38.3.4.
8. Configure GDMA outlink, see Chapter 5 VDMA Controller (VDMA).
9. Start transmitting data:

    - Wait till LCD slave gets ready.
    - Set `LCD_CAM_LCD_START` to start transmitting data.

10. Wait for the interrupt signals set in Step 3.
11. In frame intervals during data transmission, check if `LCD_CAM_LCD_NEXT_FRAME_EN` is set:
    - If yes, set `LCD_CAM_LCD_UPDATE` (repeating the steps above) to continue transmitting next frame.
    - If not, LCD stops transmitting data.
12. Clear `LCD_CAM_LCD_START` if data transmission is done.

### 38.5.2 Configure LCD (I8080/MOTO6800 Format) as TX Mode

Follow the steps below to configure LCD (I8080/MOTO6800 format) as TX mode via software:

1. Configure clock according to Section 38.3.3.
```