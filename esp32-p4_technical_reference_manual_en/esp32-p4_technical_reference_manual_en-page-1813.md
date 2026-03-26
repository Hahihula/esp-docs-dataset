
```markdown
- The pixel clock frequency must be less than 40 MHz.
- If YUV-RGB format conversion is being used at the same time, the pixel clock frequency must be less than 30 MHz.

## 38.5.3 Configure Camera as RX Mode

Follow the steps below to configure the Camera as RX mode via software:

1. Configure clock according to Section 38.3.3. Note that in slave mode, the module clock frequency should be twice as fast as the PCLK frequency of the image sensor.
2. Configure signal pins according to Table 38.3-1 and Chapter 9 GPIO Matrix and IO MUX.
3. Set or clear `LCD_CAM_CAM_VH_DE_MODE_EN` according to the control signal HSYNC.
4. Set needed RX data format according to Section 38.3.5.2.
5. Set `LCD_CAM_CAM_UPDATE` so that the configurations take effect.
6. Reset RX control unit (Camera_Ctrl) and Async RX FIFO as described in Section 38.3.4.
7. Enable corresponding interrupts, see Section 38.4.
8. Configure GDMA inlink, and set the length of RX data in `LCD_CAM_CAM_REC_DATA_BYTELEN`.
9. Start receiving data:

    - In master mode, when the slave is ready, set `LCD_CAM_CAM_START` to start receiving data.
    - In slave mode, set `LCD_CAM_CAM_START`. Receiving data starts after the master provides clock signal and control signal.

10. Receive data and store the data to GDMA. Then corresponding interrupts set in Step 7 will be generated.

**Notes:**

- No matter in which operation mode, camera master RX mode or camera slave RX mode, the rules below must be followed when accessing internal memory via GDMA:

    - If 8-bit parallel data input mode is selected, then

        * The pixel clock frequency must be less than 80 MHz.
        * If YUV-RGB format is being used at the same time, the pixel clock frequency must be less than 60 MHz.

    - If 16-bit parallel data input mode is selected, then

        * The pixel clock frequency must be less than 40 MHz.
        * If YUV-RGB format conversion is being used at the same time, the pixel clock frequency must be less than 30 MHz.

**Note:**

If both LCD and camera are connected externally at the same time, it is necessary to ensure that the maximum data throughput on the interface is less than the total data bandwidth of GDMA when accessing internal/external storage. The default frequency of APB_CLK is 80 MHz in this scenario. For more information about APB_CLK, see Chapter 10 *Reset and Clock*.
```