
```markdown
| Color Space Conversion Method | INPUT_SEL_CHO | 3B_PROC_EN_CHO | OUTPUT_SEL_CHO |
|-------------------------------|---------------|-----------------|----------------|
| YUV420 → RGB                  | 0             | 1               | 1              |
| YUV422 → RGB                  | 0             | 1               | 1              |
| YUV444 → RGB                  | 2             | 1               | 1              |
| YUV444 (only reverse the pixel order) | 2           | 0               | 1              |
| No color space conversion     | 7             | N/A             | N/A            |

Note that, this function is only available for 2D DMA RX channel0, not for any other RX channels.

(j) Configure parameters required for the color space conversion formula, including
DMA2D_IN_COLOR_PARAM_HO_CHO, DMA2D_IN_COLOR_PARAM_H1_CHO,
DMA2D_IN_COLOR_PARAM_MO_CHO, DMA2D_IN_COLOR_PARAM_M1_CHO,
DMA2D_IN_COLOR_PARAM_LO_CHO, and DMA2D_IN_COLOR_PARAM_L1_CHO. Note that, this function is only available for 2D DMA RX channel0, not for any other RX channels.

(k) Select whether to reverse the pixel order of the image after 2D DMA color space conversion by configuring DMA2D_IN_SCRAMBLE_SEL_POST_CHO:
*   0: BYTE2-1-O
*   1: BYTE2-O-1
*   2: BYTE1-O-2
*   3: BYTE1-2-O
*   4: BYTEO-2-1
*   5: BYTEO-1-2

Configuration of 5 means reversing the pixel order, for example, reversing the RGB after 2D DMA color space conversion to BGR. Note that, this function is only available for 2D DMA RX channel0, not for any other RX channels.

(l) Configure DMA2D_OUTLINK_ADDR_CHn as the 2D DMA TX channel linked list address, configure DMA2D_INLINK_ADDR_CHn as the 2D DMA RX channel linked list address.

4. Enable interrupt sources:
*   DMA2D_OUT_INT_ENA_CHn_REG
*   DMA2D_IN_INT_ENA_CHn_REG
*   JPEG_INT_ENA_REG

5. Start the transmission of 2D DMA channels:
*   2D DMA TX channeln: set DMA2D_OUTLINK_START_CHn to 1 and then to 0
*   2D DMA RX channeln: set DMA2D_INLINK_START_CHn to 1 and then to 0

6. Start JPEG codec decoding by setting the JPEG_JPEG_START field.

7. Wait till DMA2D_IN_SUC_EOF_CHn_INT becomes 1, indicating that the decoded image has been completely written to the memory.
```