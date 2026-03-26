

```markdown
4. Configure MIPI CSI HOST according to Chapter 40 MIPI CSI;
5. Configure ISP general settings as described in Section 36.7.4;
6. Select the input source as MIPI-CSI by setting `ISP_IN_SRC` to 0;
7. Configure the input data type via `ISP_DATA_TYPE`;
8. Enable the ISP by setting `ISP_EN` to 1;
9. Enable MIPI-CSI data input by setting `ISPI_MIPI_DATA_EN` to 1.

## 36.7.6 Enabling ISP for Image Capture from DVP

1. Configure ISP and CSI_Bridge clocks and reset as described in Section 36.7.1;
2. Configure CSI_Bridge as described in Section 36.7.2;
3. Configure VDMA as described in Section 36.7.3;
4. Configure ISP general settings as described in Section 36.7.4;
5. Select the input source as DVP by setting `ISP_IN_SRC` to 1;
6. Configure the input data type via `ISP_CAM_DATA_TYPE`, and write 0 to `ISP_DATA_TYPE`;
7. Enable the ISP by setting `ISP_EN` to 1;
8. Configure the data mode for DVP interface via `ISP_CAM_CONF_REG`;
9. Reset the DVP interface by setting `ISP_CAM_RESET` to 1, waiting for a period, then setting it to 0;
10. Write 1 to `ISP_CAM_UPDATE_REG`;
11. Enable the DVP interface by setting `ISP_CAM_EN` to 1;
12. Wait for `ISP_CAM_UPDATE_REG` to automatically clear for initialization.

## 36.7.7 Enabling ISP for Image Capture from VDMA

1. Configure ISP and CSI_Bridge clocks and reset as described in Section 36.7.1;
2. Configure CSI_Bridge as described in Section 36.7.2;
3. Configure VDMA as described in Section 36.7.3;
4. Configure ISP general settings as described in Section 36.7.4;
5. Select the input source as VDMA by setting `ISP_IN_SRC` to 2;
6. Configure the input data type via `ISP_DMA_DATA_TYPE` and `ISP_DATA_TYPE`;
7. Configure the total amount of raw image data for one frame in “64-bit” units using `ISP_DMA_RAW_NUM_TOTAL`, which value should equal image width x image height x bits per pixel/64. Then, write 1 to `ISP_DMA_RAW_NUM_TOTAL_SET` to activate the configuration;
8. Configure the burst length via `ISP_DMA_BURST_LEN`, which needs to align with the VDMA configuration;
9. Write 1 to `ISP_DMA_UPDATE_REG` to update the VDMA configuration, and wait for the update to complete;
10. Send a frame of data by setting `ISP_DMA_EN` to 1.
```