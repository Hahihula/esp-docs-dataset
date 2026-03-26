

```markdown
Register 35.18. JPEG_INT_CLR_REG (0x0044)

Continued from the previous page...

JPEG_UXP_DET_INT_CLR    Write 1 to clear JPEG_UXP_DET_INT. (WT)
JPEG_EN_FRAME_EOF_ERR_INT_CLR   Write 1 to clear JPEG_EN_FRAME_EOF_ERR_INT. (WT)
JPEG_EN_FRAME_EOF_LACK_INT_CLR  Write 1 to clear JPEG_EN_FRAME_EOF_LACK_INT. (WT)
JPEG_DE_FRAME_EOF_ERR_INT_CLR   Write 1 to clear JPEG_DE_FRAME_EOF_ERR_INT. (WT)
JPEG_DE_FRAME_EOF_LACK_INT_CLR  Write 1 to clear JPEG_DE_FRAME_EOF_LACK_INT. (WT)
JPEG_SOS_UNMATCH_ERR_INT_CLR    Write 1 to clear JPEG_SOS_UNMATCH_ERR_INT. (WT)
JPEG_MARKER_ERR_FST_SCAN_INT_CLR   Write 1 to clear JPEG_MARKER_ERR_FST_SCAN_INT. (WT)
JPEG_MARKER_ERR_OTHER_SCAN_INT_CLR Write 1 to clear JPEG_MARKER_ERR_OTHER_SCAN_INT. (WT)
JPEG_UNDET_INT_CLR    Write 1 to clear JPEG_UNDET_INT. (WT)
JPEG_DECODE_TIMEOUT_INT_CLR   Write 1 to clear JPEG_DECODE_TIMEOUT_INT. (WT)

Register 35.19. JPEG_DHT_TOTLEN_DCO_REG (0x0058)


| 31                                                                 | 0 |
|--------------------------------------------------------------------|----|
|                                                                    |    |
| 0x000000                                                           | Reset |

JPEG_DHT_TOTLEN_DCO   Configures the number of codeword with a codeword length of 1 to 16 bits for DCO Huffman table in FIFO mode. (HRO)
```