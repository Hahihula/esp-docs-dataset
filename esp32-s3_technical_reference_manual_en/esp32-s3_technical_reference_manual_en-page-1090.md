**Title: Chapter 29 LCD and Camera Controller (LCD_CAM)**

- **GoBack**

13. Wait for the interrupt signals set in Step 3.
14. Clear `LCD_CAM_LCD_START` if data transmission is done.

**Notes:**  
No matter in which format, RGB or I8080/MOTO6800, the rules below must be followed when accessing internal memory via GDMA:

- If LCD data bus is configured to 8-bit parallel output mode, then
  - pixel clock frequency must be less than 80 MHz.
  - if YUV-RGB format conversion is used meanwhile, the pixel clock frequency must be less than 60 MHz.

- If LCD data bus is configured to 16-bit parallel output mode, then
  - pixel clock frequency must be less than 40 MHz.  
  - if YUV-RGB format conversion is used meanwhile, the pixel clock frequency must be less than 30 MHz.

**Subtitle: 29.4.3 Configure Camera as RX Mode**

Follow the steps below to configure camera as RX mode via software:

1. **Configure clock according to Section 29.3.3.** Note that in slave mode, the module clock frequency should be two times faster than the PCLK frequency of the image sensor.
2. **Configure signal pins according to Table 29.3-1.**
3. Set or clear `LCD_CAM_CAM_VH_DE_MODE_EN` according to the control signal HSYNC.
4. Set needed RX channel mode and RX data mode, then set the bit `LCD_CAM_CAM_UPDATE`.
5. Reset RX control unit (Camera, Ctrl) and Async Rx FIFO as described in Section 29.3.4.
6. Enable corresponding interrupts, see Section 29.5.
7. Configure GDMA inlink, and set the length of RX data in `LCD_CAM_CAM_REC_DATA_BYTLEEN`.
8. Start receiving data:
   - In master mode, when the slave is ready, set `LCD_CAM_CAM_START` to start receiving data.
   - In slave mode, set `LCD_CAM_CAM_START`. Receiving data starts after the master provides clock signal and control signal.

9. Receive data and store the data to the specified address of ESP32-S3 memory. Then corresponding interrupts in Step 6 will be generated.

**Notes:**  
No matter in which operation mode, camera master RX mode or camera slave RX mode, the rules below must be followed when accessing internal memory via GDMA:
- If 8-bit parallel data input mode is selected, then
  - pixel clock frequency must be less than 80 MHz.  

---

**Footer:**
Espressif Systems  
1090  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback