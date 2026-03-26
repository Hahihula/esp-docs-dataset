

```markdown
- Baseline profile and level 4.1.
- 8-bit YUV 4:2:0 progressive video with a maximum resolution of 1920 × 1088 @ 30fps.
- I and P frames.
- Two working modes: GOP mode and dual stream mode. In dual stream mode, the total bandwidth of the two video sequences to be encoded should not exceed 1920 x 1088 @ 30fps.
- 4 x 4 and 16 x 16 intra frame luma MB segmentation.
- All 9 prediction modes for intra 4 x 4 luma MBs, and all 4 prediction modes for intra 16 x 16 luma MBs.
- All 4 prediction modes for intra chroma MBs.
- All partition size for inter luma MBs: 4 x 4, 4 x 8, 8 x 4, 8 x 8, 8 x 16, 16 x 8, 16 x 16.
- 1/2 and 1/4 pixel precision motion estimation.
- Horizontal motion search range [-29.75, +16.75] and vertical motion search range [-13.75, +13.75].
- Deblocking filter.
- CAVLC.
- P-skip MBs.
- I MB in P slices.
- Decimation operation of luma and chroma component quantization results.
- Fixed QP and MB level rate control.
- MV merge function. If the MV of MB is greater than 0, it can be output to memory.
- ROI function, with up to 8 rectangular ROI configurable at any position (allowing overlap, fixed priority). Each ROI can be configured with a constant QP or QP offset, and non-ROI can be configured with a QP offset.

## 39.4 Architecture

The architecture of H264 is shown in Figure 39.4-1.
```