

```markdown
- Wait for the ISP interrupt triggered by AE_MONITOR_INT
- Or query the status using ISP_AE_MONITOR_INT_RAW
- After detecting a change in luminance, disable luminance monitoring, re-initiate camera exposure, and then re-enable monitoring

## 36.7.10 AF Configuration

AF can be configured after the ISP is enabled as follows:

1. Set up three statistical windows A, B, and C, ensuring each window does not exceed 1024 x 1024;
   - Set the left boundary using `ISP_AF_LPOINT_A/B/C`
   - Set the right boundary using `ISP_AF_RPOINT_A/B/C`
   - Set the top boundary using `ISP_AF_TPOINT_A/B/C`
   - Set the bottom boundary using `ISP_AF_BPOINT_A/B/C`

2. Set the sharpness threshold via `ISP_AF_THRESHOLD`;

3. Configure focus scene monitoring;
   - If focus scene monitoring is required, set the monitoring period `ISP_AF_ENV_PERIOD` to a non-zero value
   - There are two ways to set the threshold
     - If `ISP_AF_ENV_USER_THRESHOLD_SUM` or `ISP_AF_ENV_USER_THRESHOLD_LUM` is non-zero, use the specified values as thresholds for sharpness and brightness changes
     - If `ISP_AF_ENV_USER_THRESHOLD_SUM` or `ISP_AF_ENV_USER_THRESHOLD_LUM` is zero, use the sharpness and brightness of the most recent statistics multiplied by `ISP_AF_ENV_THRESHOLD` (4 fractional bits) as the change threshold

4. Configure the statistical trigger mode. After each trigger completes, update the monitoring baseline;
   - If `ISP_AF_AUTO_UPDATE` is 1, it is in automatic triggering mode, which performs statistics for every frame with AF enabled. Since each statistical calculation clears the frame count for monitoring, the monitoring will be disabled
   - If `ISP_AF_AUTO_UPDATE` is 0, it is in manual triggering mode. The monitoring is working only under this condition

5. Enable AF by writing 1 to `ISP_AF_EN`;

6. Obtain statistics;
   - Clear the completion status by writing 1 to `ISP_AF_FDONE_INT_CLR`
   - Trigger statistics
     - With automatic triggering, statistics are performed for every frame
     - With manual triggering, write 1 to `ISP_AF_MANUAL_UPDATE` to trigger statistics manually
   - Wait for the statistics to complete
     - Wait for the ISP interrupt triggered by AF_FDONE_INT.
```