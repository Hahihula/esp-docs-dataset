

```markdown
Chapter 36 Image Signal Processor (ISP) GoBack

## 36.712 HIST Configuration

HIST can be configured after the ISP is enabled.

1. Select sampling points via `ISP_HIST_MODE`;
   - If sampling points are set to RGB, use `ISP_HIST_COEFF_R/G/B` to set RGB weights with 8 fractional bits
2. Set up statistical windows;
   - Set the horizontal start point with `ISP_HIST_X_OFFS`
   - Configure the horizontal dimension of each sub-window with `ISP_HIST_X_SIZE`
   - Set the vertical start point with `ISP_HIST_Y_OFFS`
   - Configure the vertical dimension of each sub-window with `ISP_HIST_Y_SIZE`
3. Configure histograms;
   - Set histogram interval divisions using `ISP_HIST_SEG_X_x`
   - Set window weights using `ISP_HIST_WEIGHT_xx` with 8 fractional bits
4. Enable HIST by writing 1 to `ISP_HIST_EN`;
5. Obtain statistics.
   - Clear the completion status by writing 1 to `ISP_HIST_FDONE_INT_CLR`
   - With HIST enabled, statistics are performed at the end of every frame. Wait for the statistics to complete
     - Wait for the ISP interrupt triggered by `HIST_FDONE_INT`
     - Or query the status using `ISP_HIST_FDONE_INT_RAW`.
   - Obtain the statistics for each interval by reading `ISP_HIST_BIN_x`.

## 36.713 ISP_Pipeline Module Update Configuration

1. Disable the module via `ISP_CNTL_REG`;
2. Wait for the interrupt from the corresponding module;
3. Update module configurations;
4. Re-enable the module.
```