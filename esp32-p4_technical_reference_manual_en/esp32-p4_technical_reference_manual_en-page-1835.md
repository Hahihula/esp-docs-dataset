

```markdown
Figure 39.4-1. H264 Video Encoder Architecture

The H264 encoder can be divided into two parts, H264 dedicated DMA (H264_DMA) and encoder algorithm core (ENC_CORE). H264_DMA is used for data transfer, and is connected to the internal/external memory through two sets of AXI buses. Meanwhile, it is connected to the ENC_CORE through multiple DMA sending/receiving channels (H264_DMA has 5 sending channels (TX channel n) and 6 receiving channels (RX channel n)). TX channel 3, TX channel 4, and RX channel 5 are the internal channels of H264_DMA, which are not connected to the ENC_CORE. The ENC_CORE is used to compress video sequences.

The function of each H264_DMA sending and receiving channel is as follows:

*   TX channel 0 sends the original picture to ENC_CORE.
*   TX channel 1 sends the reference picture to ENC_CORE.
*   TX channel 2 sends the deblocking filter intermediate data to ENC_CORE.
*   Sending channel TX channel 3 and TX channel 4 send the reference picture (i.e., the previous deblocking filtered picture) to receiving channel RX channel 5.
*   RX channel 0 and RX channel 1 send the result of the deblocking filter (i.e., reference picture) to external memory.
*   RX channel 2 sends the deblocking filter intermediate data to internal memory.
*   RX channel 3 sends the MV merge result to internal memory.
*   RX channel 4 sends the encoded bitstream to external memory.
*   RX channel 5 sends the reference picture (i.e., the previous deblocking filtered picture) to internal memory.

From the provided description, the H264_DMA channels can be divided into two types:

*   Reading or writing internal memory (through AXI_M1 bus): TX channel 1/2, RX channel 2/3/5
```