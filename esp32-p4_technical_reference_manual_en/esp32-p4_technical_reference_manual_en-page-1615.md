

```markdown
| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| **Control and Configuration registers**    |                                                                                               |           |        |
| JPEG_CONFIG_REG                           | System level control and configuration register                                              | 0x0000    | varies |
| JPEG_DQT_INFO_REG                         | Quantization coefficient table information register                                          | 0x0004    | R/W    |
| JPEG_PIC_SIZE_REG                         | Image size register                                                                          | 0x0008    | R/W    |
| JPEG_EXTD_CONFIG_REG                      | Extended color space conversion configuration register                                      | 0x000C    | R/W    |
| JPEG_TOQNR_REG                            | Quantization coefficient table0 register                                                     | 0x0010    | HRO    |
| JPEG_T1QNR_REG                             | Quantization coefficient table1 register                                                    | 0x0014    | HRO    |
| JPEG_T2QNR_REG                             | Quantization coefficient table2 register                                                    | 0x0018    | HRO    |
| JPEG_T3QNR_REG                             | Quantization coefficient table3 register                                                    | 0x001C    | HRO    |
| JPEG_DECODE_CONF_REG                      | Decoder configuration register                                                              | 0x0020    | varies |
| JPEG_C0_REG                                | Color component0 register                                                                    | 0x0024    | R/W    |
| JPEG_C1_REG                                | Color component1 register                                                                    | 0x0028    | R/W    |
| JPEG_C2_REG                                | Color component2 register                                                                    | 0x002C    | R/W    |
| JPEG_C3_REG                                | Color component3 register                                                                    | 0x0030    | R/W    |
| JPEG_DHT_INFO_REG                          | Huffman table information register                                                          | 0x0034    | R/W    |
| JPEG_DHT_TOTLEN_DCO_REG                   | DCO Huffman table codeword length register                                                  | 0x0058    | HRO    |
| JPEG_DHT_VAL_DCO_REG                       | DCO Huffman table symbol register                                                           | 0x005C    | HRO    |
| JPEG_DHT_TOTLEN_ACO_REG                   | ACO Huffman table codeword length register                                                  | 0x0060    | HRO    |
| JPEG_DHT_VAL_ACO_REG                       | ACO Huffman table symbol register                                                           | 0x0064    | HRO    |
| JPEG_DHT_TOTLEN_DC1_REG                   | DC1 Huffman table codeword length register                                                  | 0x0068    | HRO    |
| JPEG_DHT_VAL_DC1_REG                       | DC1 Huffman table symbol register                                                           | 0x006C    | HRO    |
| JPEG_DHT_TOTLEN_AC1_REG                   | AC1 Huffman table codeword length register                                                  | 0x0070    | HRO    |
| JPEG_DHT_VAL_AC1_REG                       | AC1 Huffman table symbol register                                                           | 0x0074    | HRO    |
| JPEG_DHT_CODEMIN_DCO_REG                  | DCO Huffman table minimum codeword register                                                 | 0x0078    | HRO    |
| JPEG_DHT_CODEMIN_ACO_REG                  | ACO Huffman table minimum codeword register                                                 | 0x007C    | HRO    |
| JPEG_DHT_CODEMIN_DC1_REG                  | DC1 Huffman table minimum codeword register                                                 | 0x0080    | HRO    |
| JPEG_DHT_CODEMIN_AC1_REG                  | AC1 Huffman table minimum codeword register                                                 | 0x0084    | HRO    |
| JPEG_SYS_REG                               | System configuration register                                                                | 0x00F8    | R/W    |
| **Interrupt registers**                    |                                                                                               |           |        |
| JPEG_INT_RAW_REG                           | Interrupt raw status register                                                                | 0x0038     | R/WTC/SS|
| JPEG_INT_ENA_REG                            | Interrupt enable register                                                                     | 0x003C     | R/W    |
| JPEG_INT_ST_REG                             | Interrupt masked status register                                                             | 0x0040     | RO     |
| JPEG_INT_CLR_REG                             | Interrupt clear register                                                                      | 0x0044     | WT     |
| **Version Register**                        |                                                                                               |           |        |
| JPEG_VERSION_REG                            | Version control register                                                                      | 0x00FC     | R/W    |
```