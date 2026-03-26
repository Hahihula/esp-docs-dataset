

```markdown
## 36.7.3 VDMA Configuration

1. Configure the register corresponding to the channel:

   - Set SRC/DST_MULTBLK_TYPE to 3 (configure with linked list)
   
   - Configure TT_FC
   
     - For CSI_Bridge, set TT_FC to 4 (peripheral to memory with peripheral flow control)
     
     - For memory to ISP, set TT_FC to 6 (memory to peripheral with peripheral flow control)

   - Configure HS_SEL

     - For CSI_Bridge, set HS_SEL_SRC to 0 (peripheral uses hardware handshake), and set HS_SEL_DST to 1 (memory uses software handshake)
     
     - For memory to ISP, set HS_SEL_SRC to 1 (memory uses software handshake), and set HS_SEL_DST to 0 (peripheral uses hardware handshake)

   - Assign hardware handshake channels

     - For CSI_Bridge, set SRC_PER to 1
       
     - For memory to ISP, set DST_PER to 2

   - Set SRC/DST_TR_WIDTH to 3 (data width of 64 bits)

2. Establish the linked list based on the configured registers.

**Note:**
The VDMA configuration outlined in this section covers essential steps. For detailed procedures, refer to Chapter 5 VDMA Controller (VDMA).
Ensure that image dimensions and start addresses are aligned to 8 bytes.


## 36.7.4 ISP General Configuration

1. Configure the input image size via `ISP_HADR_NUM` and `ISP_VADR_NUM`

2. Set image arrangement mode in the Bayer domain via `ISP_BAYER_MODE`;

3. Specify the ISP output data format via `ISP_OUT_TYPE`;

4. Configure each module in ISP_Pipeline. Refer to the corresponding section in 36.5.2 for details;

5. Enable the necessary Pipeline modules by setting the fields in register `ISP_CNTL_REG`. Ensure that the format conversion-related modules (Demosaic, RGB2YUV, YUV2RGB) are enabled before enabling the ISP, and that they match the final output format.


## 36.7.5 Enabling ISP for Image Capture from MIPI-CSI

1. Configure ISP and CSI_Bridge clocks and reset as described in Section 36.7.1;

2. Configure CSI_Bridge as described in Section 36.7.2;

3. Configure VDMA as described in Section 36.7.3;
```