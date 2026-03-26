

```markdown
Chapter 37 Pixel-Processing Accelerator (PPA) GoBack

5. Configure BLEND parameters:
* Configure the output data format of BLEND via PPA_BLEND_TX_CM
* Write 1 to PPA_BLEND_FIX_PIXEL_FILL_EN to enable image filling
* Configure the pixel value for image filling via PPA_BLEND_TX_FIX_PIXEL
* Configure the filled image size via PPA_BLEND_HB and PPA_BLEND_VB

6. Write 1 to PPA_BLEND_TRANS_MODE_UPDATE to start BLEND workflow.

37.7.6 Error Handling

- Refer to Section 37.7.1 to reset the whole PPA, and configure again.
- Or write 1 and then 0 to reset SRM and BLEND via PPA_SCAL_ROTATE_RST, PPA_BLEND_RST, and configure again.

Note:
* The 2D-DMA configurations mentioned in this chapter involve only key steps. For detailed procedures, please refer to 6 2D-DMA Controller (2D-DMA).
* In this chapter, DMA2D_OUT corresponds to the PPA input direction, and DMA2D_IN corresponds to the PPA output direction.
```