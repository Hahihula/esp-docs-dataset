

```markdown
Register 35.9. JPEG_DECODE_CONF_REG (0x0020)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | JPEG_DEZIGZAG_READY_CTL                                                     |
| 29  | JPEG_MULTI_SCAN_ERR_CHECK                                                   |
| 28  | JPEG_RST_CHECK_BYTE_NUM                                                     |
| 27  | JPEG_SOS_CHECK_BYTE_NUM                                                     |
| 26  | JPEG_SW_DHT_EN                                                               |
| 25  | JPEG_COMPONENT_NUM                                                           |
| 24  | JPEG_SW_DHT_EN                                                               |
| 23  | JPEG_SOS_CHECK_BYTE_NUM                                                     |
| 16-0| JPEG_RESTART_INTERVAL                                                       |

Value on reset: 0x00

JPEG_RESTART_INTERVAL Configures the RST interval in DRI segment when decoding. (R/W)

JPEG_COMPONENT_NUM Configures the number of chrominance components in the image when decoding. (R/W)

JPEG_SW_DHT_EN Represents the Huffman table configured by the software for the decoder. The value is always 1. (RO)

JPEG_SOS_CHECK_BYTE_NUM Configures the byte number to check the next SOS marker in the multi-scan image after one scan is decoded down. The actual check number is JPEG_SOS_CHECK_BYTE_NUM + 1 (R/W)

JPEG_RST_CHECK_BYTE_NUM Configures the byte number to check the next RST marker after one RST interval is decoded down. The actual check number is JPEG_RST_CHECK_BYTE_NUM + 1. (R/W)

JPEG_MULTI_SCAN_ERR_CHECK Reserved for decoder and should not be configured. (R/W)

JPEG_DEZIGZAG_READY_CTL Reserved for decoder and should not be configured. (R/W)
```