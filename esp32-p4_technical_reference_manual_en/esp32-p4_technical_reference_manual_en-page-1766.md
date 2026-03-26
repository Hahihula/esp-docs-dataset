

```markdown
- Initialize the CLUT by writing data directly to the corresponding address, referring to Table 37.5-3
```

## 37.7.4 BLEND Configuration

1. Refer to Section 37.7.1 to enable and reset PPA and 2D-DMA.

2. Configure the input and output link lists of 2D-DMA. For detailed parameters, please refer to Table 37.5-4.

3. Select the input and output channels of 2D-DMA:

   - Write 0x2 to `DMA2D_OUT_PERI_SEL_CHx` to allocate one 2D-DMA output channel to PPA BLEND for background layer input
   - Write 0x3 to `DMA2D_OUT_PERI_SEL_CHx` to allocate one 2D-DMA output channel to PPA BLEND for foreground layer input
   - Write 0x2 to `DMA2D_IN_PERI_SEL_CHx` to allocate one 2D-DMA input channel to PPA BLEND for output

4. Enable the input and output channels for 2D-DMA. The x in the registers refers to the two channels allocated to BLEND foreground and background respectively:

   - Write 1 to `DMA2D_OUTLINK_START_CHx` to enable the output channel of 2D-DMA
   - Write 1 to `DMA2D_INLINK_START_CHx` to enable the input channel of 2D-DMA

5. Configure BLEND parameter:

   - Configure the data type for the background layer input of BLEND via `PPA_BLENDO_RX_CM`. If the format is L4/L8, initialize the CLUT first as described in 37.7.3
   - Configure the data type for the background layer input of BLEND via `PPA_BLEND1_RX_CM`. If the format is L4/L8, initialize the CLUT first as described in 37.7.3
   - Configure the output data format of BLEND via `PPA_BLEND_TX_CM`
   - Configure the upper and lower limits of the color-key for the background layer via `PPA_CK_BG_HIGH_REG` and `PPA_CK_BG_LOW_REG`
   - Configure the upper and lower limits of the color-key for the foreground layer via `PPA_CK_FG_HIGH_REG` and `PPA_CK_FG_LOW_REG`
   - Configure the default value and behavior for the color-key via `PPA_CK_DEFAULT_REG`
   - Write 1 to `PPA_BLEND_EN` to enable BLEND

6. Write 1 to `PPA_BLEND_TRANS_MODE_UPDATE` to start BLEND workflow

## 37.7.5 BLEND Image Filling Configuration

1. Refer to Section 37.7.1 to enable and reset PPA and 2D-DMA.

2. Configure the input link lists of 2D-DMA (output link lists of PPA BLEND). For detailed parameters, please refer to Table 37.5-4.

3. Write 0x2 to `DMA2D_IN_PERI_SEL_CHx` to allocate one 2D-DMA input channel to PPA BLEND output.

4. Write 1 to `DMA2D_INLINK_START_CHx` to enable the output channel of 2D-DMA.
```