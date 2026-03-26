

```markdown
## 36.7.8 LSC LUT Configuration

LSC can be configured after the ISP is enabled. Before enabling LSC, initialize the LSC LUT as follows:

1. Write to LUT:
   - Write the data to be stored in the LUT by writing to `ISP_LUT_WDATA_REG`
   - Store the data at the specified address by writing to `ISP_LUT_CMD_REG`

2. Read from LUT.
   - Retrieve the data stored at the specified address by writing to `ISP_LUT_CMD_REG`
   - Obtain the data read from the LUT by reading from `ISP_LUT_RDATA_REG`

## 36.7.9 AE Configuration

AE can be configured after the ISP is enabled as follows:

1. Select sampling points via `ISP_AE_SELECT`;

2. Set up statistical windows:
   - Set the horizontal starting point with `ISP_AE_X_START`
   - Configure the horizontal dimension of each sub-window with `ISP_AE_X_BSIZE`
   - Set the vertical starting point with `ISP_AE_Y_START`
   - Configure the vertical dimension of each sub-window with `ISP_AE_Y_BSIZE`
   - Specify the number of pixels in each sub-window with `ISP_AE_SUBWIN_PIXNUM`
   - Set the reciprocal of the number of pixels in each sub-window with `ISP_AE_SUBWIN_RECIP` (20 fractional bits)

3. Enable luminance monitoring:
   - If monitoring is required, set `ISP_AE_MONITOR_TH` and `ISP_AE_MONITOR_TL` to non-zero values
   - Specify the monitoring statistical period in frames via `ISP_AE_MONITOR_PERIOD`

4. Enable AE by writing 1 to `ISP_AE_EN`;

5. Obtain statistics:
   - Clear the completion status by writing 1 to `ISP_AE_FRAME_DONE_INT_CLR`
   - Initiate statistics by writing 1 to `ISP_AE_UPDATE`. Each write to this register resets the frame count for monitoring. It is recommended to disable monitoring before manual statistics and re-enable it after completion to prevent automatic results from overwriting manual results prematurely
   - Wait for the statistics to complete
     - Wait for the ISP interrupt triggered by `AE_FDONE_INT`
     - Or query the status using `ISP_AE_FRAME_DONE_INT_RAW`
   - Obtain statistics for each sub-window by reading `ISP_AE_Bxx_MEAN`

6. Perform luminance monitoring.
```