

```markdown
Figure 37.5-4. SRM Procedure


37.5.3.2 Pixel Block Rearrangement

When the output pixel block is small, initiating a 2D-DMA transfer for each pixel block would result in low bus bandwidth utilization. To improve bus bandwidth utilization, SRM can cache and concatenate output pixel blocks into a larger pixel block before outputting them all at once. This feature is enabled by default and can be disabled by setting PPA_SRM_MACRO_BK_RO_BYPASS to 1.

Once pixel block rearrangement is enabled, under certain conditions, the output pixel blocks will be automatically rearranged and concatenated, as specified in Table 37.5-6.

*   For the output pixel block in ARGB8888/RGB888 format, if its vertical height is less than or equal to 32, and the horizontal width is less than or equal to 16, pixel block rearrangement will be automatically enabled.
*   For the output pixel block in RGB565 format, if its vertical height is less than or equal to 32, and the horizontal width is less than or equal to 32, pixel block rearrangement will be automatically enabled.
*   For the output pixel block in YUV420 format, if its vertical height is less than or equal to 32, and horizontal width is less than or equal to 32, pixel block rearrangement will be automatically enabled.

Table 37.5-6. Number of Pixel Block Rearrangements in SRM Output

| ARGB8888/RGB888 Horizontal Size | Rearranger Number | Rearranger Horizontal Size | RGB565 Horizontal Size | Rearranger Number | YUV420 Horizontal Size (Even) | Rearrangement Number |
|--- | --- | --- | --- | --- | --- | ---|
| 1 | 32 | 1 | 64 | 2 | 32 |
| 2 | 16 | 2 | 32 | 4 | 16 |
| 3 | 10 | 3 | 20 | 6 | 10 |
| 4 | 8 | 4 | 16 | 8 | 8 |
| 5 | 6 | 5 | 12 | 10 | 6 |
| 6 | 5 | 6 | 10 | 12 | 5 |
| 7 | 4 | 7 | 9 | 14 | 4 |

Continued on the next page...
```