

```markdown
fractional motion estimation on the basis of the integer motion estimation. The fractional motion estimation result is sent to the mc module, and the inter prediction cost is sent to the rdo module.

*   mc: Receives the original picture MB from the cur_mb module, receives the reference picture MB from the fetch module, receives the fractional motion estimation result from the fme module, performs motion compensation according to the fractional motion estimation result. The inter-frame prediction and the sum of the residual results are sent to the trans_quant_decimate module, and the motion vector is sent to the mv_merge module.
*   rdo: Receives the intra-frame prediction cost from the intra module, receives the inter-frame prediction cost from the fme module, selects the final type of the current MB, implements the P slice to support the I MB function, and sends the final MB type to trans_quant_decimate module.
*   trans_quant_decimate: Receives the final MB type from the rdo module, receives the intra prediction and residual results from the intra module, receives the inter prediction and residual results from the mc module. Then, it performs DCT, quantization, inverse quantization, and inverse DCT, and quantization result decimation, sends the residual information to the rate_ctrl module, sends the reduced quantization result to the cavlc module, and sends the reconstruction result to the deblock module.
*   cavlc: Receives the quantization result from the trans_quant_decimate module and the prediction information of the current MB, performs context adaptive variable length coding (CAVLC), and writes the coded stream to the RX channel 4 of H264_DMA.
*   deblock: Receives reconstruction result from the trans_quant_decimate module and the prediction information of the current MB, performs deblocking filtering, and writes the deblocking filter result (i.e., the reference picture) to the RX channel 0 (rx_push_db_12line) and RX channel 1 (rx_push_db_4line). This module reads and writes the deblocking filter intermediate data through the TX channel 2 channel (tx_pop_db_tmp) and RX channel 2 channel (rx_push_db_tmp) of H264_DMA.
*   mv_merge: Receives the motion vector from the mc module, performs MV merging, and writes the merging result (MB motion information) to the RX channel 3 channel (rx_push_mv_merge) of H264_DMA.
*   rate_ctrl: Receives the residual information from the trans_quant_decimate module, receives the encoding information from the cavlc module, receives the frame-level information configured by the register module, performs MB level rate control, and converts the calculated quantization parameter (QP) to the roi module.
*   roi: Receives QPs from the rate_ctrl module, receives the ROI information configured by the register module, adjusts the QPs, and uses the adjusted QPs to process the current MB.

### 39.5.1.2 Quantization Result Decimation

The ENC_CORE calculates the score of each MB based on the magnitude of its final quantization result, and then compares the score with the configurable threshold register. If it is below the threshold, the quantization result will be set to 0. Otherwise, the quantization result will remain unchanged, so as to further improve the compression ratio. For each MB, its luma and chroma component carry out the above process independently. Different types of MBs have different comparison methods, as follows:

*   luma component I MB with 16 x 16 partition:
    ```markdown
    I_score_mb_cmp + H264_x_I16x16_DECSCORE_OFFSET < H264_x_L_DECSCORE
    ```
```