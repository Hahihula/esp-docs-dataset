
```markdown
- JPEG_C_DHT_AC_ID_ERR_INT: Triggered when the decoded AC Huffman table ID of each component is not the software configured ACO Huffman table ID or AC1 Huffman table ID.
- JPEG_C_DQT_ID_ERR_INT: Triggered when the decoded quantization table ID of each component is different from the software configured quantization table ID.
- JPEG_RST_UXP_ERR_INT: Triggered when the JPEG_RESTART_INTERVAL configured by the software is 0 but the RST marker is parsed by the decoder.
- JPEG_RST_CHECK_NONE_ERR_INT: Triggered when the JPEG_RESTART_INTERVAL configured by the software is non-0 but the RST marker cannot be parsed by the decoder.
- JPEG_RST_CHECK_POS_ERR_INT: Triggered when the MCU number between two parsed RST markers is not equal to the JPEG_RESTART_INTERVAL configured by the software.
- JPEG_OUT_EOF_INT: Triggered when the EOF marker is read from the TX channel of 2D DMA.
- JPEG_SR_COLOR_MODE_ERR_INT: This interrupt is invalid.
- JPEG_DCT_DONE_INT: Triggered when the DCT or IDCT calculation of one data unit is completed.
- JPEG_BS_LAST_BLOCK_EOF_INT: Triggered when the encoding of the last data unit is completed.
- JPEG_SCAN_CHECK_NONE_ERR_INT: Triggered when an image frame has multiple scans to be decoded and the SOS marker is not parsed within (JPEG_SOS_CHECK_BYTE_NUM + 1) bytes in any scan header information.
- JPEG_SCAN_CHECK_POS_ERR_INT: Triggered when the position of the scan header information parsed by the decoder is wrong.
- JPEG_UXP_DET_INT: Triggered when the marker parsed by the decoder is not supported by the hardware.
- JPEG_EN_FRAME_EOF_ERR_INT: Triggered when the number of data units to be encoded read from 2D DMA is less than the number of data units calculated based on the image resolution configured by the software.
- JPEG_EN_FRAME_EOF_LACK_INT: Triggered when a frame of image to be encoded is completely read from 2D DMA but the EOF marker is not read.
- JPEG_DE_FRAME_EOF_ERR_INT: Triggered when the number of data units obtained after decoding a frame of image is different from the number of data units calculated based on the image resolution configured by the software.
- JPEG_DE_FRAME_EOF_LACK_INT: Triggered when the bitstream of a image is completely read from 2D DMA but the EOF marker or EOI marker is not read.
- JPEG_SOS_UNMATCH_ERR_INT: Triggered when the number of components in the scan header information parsed by the decoder is 0 or the header length in the scan header information parsed by the decoder does not match the actual header length.
- JPEG_MARKER_ERR_FST_SCAN_INT: Triggered when there is an error in the first scan header information parsed by the decoder. The errors include errors triggering JPEG_CID_ERR_INT, errors triggering JPEG_C_DHT_DC_ID_ERR_INT, errors triggering JPEG_C_DHT_AC_ID_ERR_INT, errors triggering JPEG_C_DQT_ID_ERR_INT and errors triggering JPEG_SOS_UNMATCH_ERR_INT.
```