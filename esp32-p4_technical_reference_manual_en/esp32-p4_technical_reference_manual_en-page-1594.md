

```markdown
Figure 35.1-1. JPEG Bitstream Format


The marker code assignments are shown in Table 35.1-2.

Table 35.1-2. Marker Code Assignments

| Code Assignment | Marker   | Description                                                                 |
|-----------------|----------|-----------------------------------------------------------------------------|
| 0xFFC0          | SOFO     | Start of frame (Baseline DCT)                                               |
| 0xFFC4          | DHT      | Define Huffman table(s)                                                     |
| 0xFFDm          | RSTm     | Restart with modulo 8 count "m"                                             |
| 0xFFD8          | SOI       | Start of image                                                              |
| 0xFFD9          | EOI       | End of image                                                                |
| 0xFFDA          | SOS       | Start of scan                                                               |
| 0xFFDB          | DQT       | Define quantization table(s)                                                |
| 0xFFDD          | DRI       | Define restart interval                                                     |
| 0xFFEn          | APPn      | Reserved for application segments, "n" is 0 to F                            |
| 0xFFFE          | COM       | Comment                                                                     |

35.2 Introduction

The JPEG codec is based on the JPEG baseline standard, which specifies that an encoding process is completed through one or more scans. An scan contains one or more MCUs. MCU is the sequence of data units defined by the sampling factors of the image components in the scan, which means MCU of different image formats contains different sequence of data units, as shown in Table 35.2-1.

Table 35.2-1. The Number of Data Units in the MCU of Different Image Format

| Image Format | Luminance Component Y | Chrominance Component U | Chrominance Component V |
|--------------|------------------------|--------------------------|--------------------------|
| YUV444       | 1 x 1                  | 1 x 1                    | 1 x 1                    |
```