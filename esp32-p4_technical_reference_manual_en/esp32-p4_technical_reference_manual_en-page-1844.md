

```markdown
|31|30|29|28|27|14|13|0|
|:----|:----|:----|:----|:----|:----|:----|:----|
|owner|eof|2DEN|err_eof|length[13:0]/HB|size[13:0]/VB||
||Reserved[1:0]|mod|length[28:14]/HA|size[27:14]/VA||
||||Buffer address pointer||
||||Next descriptor address||

Figure 39.5-3. H264_DMA linked list descriptor
```

*   `owner`: Indicates the operators allowed by the buffer corresponding to the current descriptor.
    -   0: Allow the operator to be CPU.
    -   1: The operator is allowed to be H264_DMA. H264_DMA will clear this bit after using the descriptor.
        -   For transmit descriptors, since a descriptor will not be written back by default, the default owner will not be cleared. The user needs to configure H264_DMA_OUT_AUTO_WRBACK to enable writeback.

*   `eof`: End flag.
    -   0: The current descriptor is not the last descriptor.
    -   1: The current descriptor is the last descriptor.

*   `mod`: Data block read mode.
    -   0: H264_DMA read/write a picture block with a horizontal width of hb and a vertical height of vb only once.
    -   1: H264_DMA read/write multiple times the picture block with a horizontal width of hb and a vertical height of vb until the picture data with a horizontal width of HA and a vertical height of VA is read/written. Note: The unit of hb/vb/HA/VA is pixel.
        -   In 1D mode, this field must be 0.

*   `err_eof`: Receives end error flag.
    -   For the receive descriptor, the hardware will set this bit to 1 after receiving a packet and detecting a received data error.
    -   For transmit descriptors, this bit is fixed to 0.

*   `2DEN`: 2D function enable signal.
    -   0: The function of H264_DMA is the same as the general DMA function. At this time, it can be used to transfer continuous data segments.
    -   1: The H264_DMA function is enabled and data is transferred according to the configured picture blocks.
```