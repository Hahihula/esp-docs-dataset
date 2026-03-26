

```markdown
Chapter 36 Image Signal Processor (ISP)

- Or query the status using ISP_AF_FDONE_INT_RAW
• Obtain sharpness statistics by reading ISP_AF_SUMA/B/C and obtain brightness statistics by reading ISP_AF_LUMA/B/C

7. Performs focus scene monitoring.
• Wait for the ISP interrupt triggered by AF_ENV_INT
• Or query the status using ISP_AF_ENV_INT_RAW
• After detecting a change in the focus scene, disable monitoring, refocus the camera, and then re-enable monitoring


36.7.11 AWB Configuration

AWB can be configured after the ISP is enabled.

1. Select sampling points via ISP_AWB_SAMPLE and write 1 to ISP_AWB_MODE;

2. Set up statistical windows;
• Set the left boundary using ISP_AWB_LPOINT
• Set the right boundary using ISP_AWB_RPOINT
• Set the top boundary using ISP_AWB_TPOINT
• Set the bottom boundary using ISP_AWB_BPOINT

3. Configure white patch constraints;
• Set maximum luminance with ISP_AWB_MAX_LUM
• Set minimum luminance with ISP_AWB_MIN_LUM
• Set maximum R/G ratio with ISP_AWB_MAX_RG (2 integer bits, 8 fractional bits)
• Set minimum R/G ratio with ISP_AWB_MIN_RG (2 integer bits, 8 fractional bits)
• Set maximum B/G ratio with ISP_AWB_MAX_BG (2 integer bits, 8 fractional bits)
• Set minimum B/G ratio with ISP_AWB_MIN_BG (2 integer bits, 8 fractional bits)

4. Obtain statistics;
• Clear the completion status by writing 1 to ISP_AWB_FDONE_INT_CLR
• Trigger statistics by writing 0 and then 1 to ISP_AWB_EN
• Wait for the statistics to complete
    - Wait for the ISP interrupt triggered by AWB_FDONE_INT
    - Or query the status using ISP_AWB_FDONE_INT_RAW
• Get the number of white patches within the statistical window by reading ISP_AWBO_WHITE_CNT
• Get the accumulated values of the R, G, B components for the white patches within the statistical window by reading ISP_AWBO_ACC_R/G/B

Espressif Systems          1658
Submit Documentation Feedback        ESP32-P4 TRM PRELIMINARY
```