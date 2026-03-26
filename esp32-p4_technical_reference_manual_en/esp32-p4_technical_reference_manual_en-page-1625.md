

```markdown
Register 35.14. JPEG_DHT_INFO_REG (0x0034)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                     |
| 30  | O                                                                             |
| 29  | O                                                                             |
| 28  | O                                                                             |
| 27  | O                                                                             |
| 26  | O                                                                             |
| 25  | O                                                                             |
| 24  | O                                                                             |
| 23  | O                                                                             |
| 22  | O                                                                             |
| 21  | O                                                                             |
| 20  | O                                                                             |
| 19  | O                                                                             |
| 18  | O                                                                             |
| 17  | O                                                                             |
| 16  | O                                                                             |
| 15  | O                                                                             |
| 14  | O                                                                             |
| 13  | O                                                                             |
| 12  | JPEG_AC1_DHT_ID                                                              |
| 11  | JPEG_ACO_DHT_ID                                                              |
| 10  | JPEG_DC1_DHT_ID                                                              |
| 9   | JPEG_DCO_DHT_ID                                                              |
| 8   | Reset                                                                        |
| 7   | O                                                                             |
| 6   | O                                                                             |
| 5   | O                                                                             |
| 4   | O                                                                             |
| 3   | O                                                                             |
| 2   | O                                                                             |
| 1   | O                                                                             |
| 0   | O                                                                             |

JPEG_DCO_DHT_ID Configures the ID of DCO Huffman table in decoder mode. (R/W)
JPEG_DC1_DHT_ID Configures the ID of DC1 Huffman table in decoder mode. (R/W)
JPEG_ACO_DHT_ID Configures the ID of ACO Huffman table in decoder mode. (R/W)
JPEG_AC1_DHT_ID Configures the ID of AC1 Huffman table in decoder mode. (R/W)

Register 35.15. JPEG_INT_RAW_REG (0x0038)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                     |
| 30  | O                                                                             |
| 29  | O                                                                             |
| 28  | O                                                                             |
| 27  | O                                                                             |
| 26  | O                                                                             |
| 25  | O                                                                             |
| 24  | JPEG_DONE_INT_RAW                                                             |
| 23  | JPEG_RLE_PARALLEL_ERR_INT_RAW                                               |
| 22  | JPEG_CID_ERR_INT_RAW                                                         |
| 21  | JPEG_C_DHT_DC_ID_ERR_INT_RAW                                                |
| 20  | JPEG_C_DHT_AC_ID_ERR_INT_RAW                                                |
| 19  | JPEG_C_DQT_ID_ERR_INT_RAW                                                    |
| 18  | JPEG_RST_UXP_ERR_INT_RAW                                                     |
| 17  | JPEG_RST_CHECK_NONE_ERR_INT_RAW                                             |
| 16  | O                                                                             |
| 15  | O                                                                             |
| 14  | O                                                                             |
| 13  | O                                                                             |
| 12  | O                                                                             |
| 11  | O                                                                             |
| 10  | O                                                                             |
| 9   | O                                                                             |
| 8   | O                                                                             |
| 7   | JPEG_DONE_INT_RAW                                                             |
| 6   | JPEG_RLE_PARALLEL_ERR_INT_RAW                                               |
| 5   | JPEG_CID_ERR_INT_RAW                                                         |
| 4   | JPEG_C_DHT_DC_ID_ERR_INT_RAW                                                |
| 3   | JPEG_C_DHT_AC_ID_ERR_INT_RAW                                                |
| 2   | JPEG_C_DQT_ID_ERR_INT_RAW                                                    |
| 1   | JPEG_RST_UXP_ERR_INT_RAW                                                     |
| 0   | JPEG_RST_CHECK_NONE_ERR_INT_RAW                                             |

JPEG_DONE_INT_RAW The raw status of JPEG_DONE_INT. (R/WTC/SS)
JPEG_RLE_PARALLEL_ERR_INT_RAW The raw status of JPEG_RLE_PARALLEL_ERR_INT.
(R/WTC/SS)
JPEG_CID_ERR_INT_RAW The raw status of JPEG_CID_ERR_INT1. (R/WTC/SS)
JPEG_C_DHT_DC_ID_ERR_INT_RAW The raw status of JPEG_C_DHT_DC_ID_ERR_INT.
(R/WTC/SS)
JPEG_C_DHT_AC_ID_ERR_INT_RAW The raw status of JPEG_C_DHT_AC_ID_ERR_INT.
(R/WTC/SS)
JPEG_C_DQT_ID_ERR_INT_RAW The raw status of JPEG_C_DQT_ID_ERR_INT. (R/WTC/SS)
JPEG_RST_UXP_ERR_INT_RAW The raw status of JPEG_RST_UXP_ERR_INT. (R/WTC/SS)
JPEG_RST_CHECK_NONE_ERR_INT_RAW The raw status of JPEG_RST_CHECK_NONE_ERR_INT.
(R/WTC/SS)

Continued on the next page...
```