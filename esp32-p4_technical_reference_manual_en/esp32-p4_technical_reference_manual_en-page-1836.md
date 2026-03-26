

```markdown
- Reading or writing external memory (through AXI_M2 bus): TX channel 0/3/4, RX channel 0/1/4


## 39.5 Functional Description

### 39.5.1 Encoder Algorithm Core (ENC_CORE)

The function of the ENC_CORE is to compress and encode the video sequences according to the software configuration.

#### 39.5.1.1 Architecture

The architecture of the encoder algorithm core is shown in Figure 39.5-1 ENC_CORE Architecture.


![Figure 39.5-1. ENC_CORE Architecture](image_path_if_available)

**Figure 39.5-1. ENC_CORE Architecture**

The functions of each module are as follows:

*   register: Implements register configuration and selection.
*   top_ctrl: Realizes the control and scheduling of each module of the encoder algorithm core.
*   cur_mb: Reads the original picture MB from the TX channel 0 (tx_pop_ori) of H264_DMA, and distributes it to the intra, ime, fme, and mc modules.
*   intra: Uses the reconstruction result calculated by the trans_quant_decimate module to perform intra-frame prediction of the MB, sends the intra-frame prediction and residual results to the trans_quant_decimate module, and sends the intra-frame prediction cost to the rdo module.
*   fetch: Reads reference picture MBs within the search range from the TX channel 1 channel (tx_pop_ref) of H264_DMA, and distributes them to the ime, fme, and mc modules.
*   ime: Receives the original picture MB from the cur_mb module, receives the reference picture MB from the fetch module, performs integer motion estimation within the search range, and sends the integer motion estimation result to the fme module.
*   fme: Receives the original picture MB from the cur_mb module, receives the reference picture MB from the fetch module, receives the integer motion estimation result from the ime module, and performs...
```