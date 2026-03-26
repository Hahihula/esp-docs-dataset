

```markdown
| ISP_RGB2YUV_FRAME_INT | After module RGB2YUV processes a frame | isp_interrupt |
|------------------------|-----------------------------------------|---------------|
| ISP_GAMMA_FRAME_INT    | After module gamma correction processes a frame | isp_interrupt |
| ISP_CCM_FRAME_INT      | After module CCM processes a frame     | isp_interrupt |
| ISP_DEMOSAIC_FRAME_INT | After module demosaic processes a frame | isp_interrupt |
| ISP_BF_FRAME_INT       | After module BF processes a frame      | isp_interrupt |
| ISP_DPC_FRAME_INT      | After module DPC processes a frame     | isp_interrupt |
| ISP_LSC_FRAME_INT      | After module LSC processes a frame     | isp_interrupt |
| ISP_BLC_FRAME_INT      | After module BLC processes a frame     | isp_interrupt |
| ISP_FRAME_INT          | After ISP_Pipeline outputs a frame     | isp_interrupt |
| ISP_HIST_FDONE_INT     | After module HIST processes a frame    | isp_interrupt |
| ISP_AWB_FDONE_INT      | After module AWB processes a frame     | isp_interrupt |
| ISP_AF_ENV_INT         | When module AF detects a change in the focus scene | isp_interrupt |
| ISP_AF_FDONE_INT       | After module AF processes a frame      | isp_interrupt |
| ISP_AE_FRAME_DONE_INT  | After module AE processes a frame      | isp_interrupt |
| ISP_AE_MONITOR_INT     | When module AE detects a change in the luminance | isp_interrupt |
| ISP_GAMMA_XCOORD_ERR_INT | When the GAMMA parameter is set incorrectly, the X length in `ISP_GAMMA_R/G/B_X00-OF` is not 256 | isp_interrupt |
| ISP_DPC_CHECK_DONE_INT | After DPC static calibration processes a frame | isp_interrupt |
| ISP_MIPI_HNUM_UNMATCH_INT | When the width HNUM settings do not match the actual input from MIPI-CSI | isp_interrupt |
| ISP_DATA_TYPE_SETTING_ERR_INT | When DATA_TYPE settings do not match the actual input data | isp_interrupt |
| ISP_HVNUM_SETTING_ERR_INT | When the width HNUM and the height VNUM settings are incorrect: Image dimensions must be even; with the RAW10 input, HNUM must be a multiple of 4 | isp_interrupt |
| ISP_BUF_FULL_INT       | When ISP_Header buffer is full           | isp_interrupt |
| ISP_ASYNC_FIFO_OVF_INT | When asynchronous FIFO of ISP_Header is overflowed | isp_interrupt |
| ISP_DATA_TYPE_ERR_INT  | When illegal DATA_TYPE is used for input data (not RAW8/RAW10/RAW12) | isp_interrupt |
| CSI_BRIG_DMA_CFG_HAS_UPDATED_INT | When VDMA configuration of CSI_Bridge is updated | csi_bridge_interrupt |
| CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT | When asynchronous FIFO of CSI_Bridge is overflowed | csi_bridge_interrupt |
| CSI_BRIG_CSI_BUF_OVERRUN_INT | When CSI_Bridge buffer is overflowed    | csi_bridge_interrupt |
```