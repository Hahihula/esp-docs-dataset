

```markdown
| JPEG_EXTD_COLOR_SPACE_EN | JPEG_COLOR_SPACE | JPEG_EXTD_COLOR_SPACE | Format¹ | JPEG_PIXEL_REV | Pixel Order |
|---------------------------|------------------|------------------------|---------|----------------|-------------|
|                           |                  |                        |         |                |             |
| 0                         | 0                | N/A                    | RGB888  | 0              | RGB         |
|                           | 1                |                        |         | 1              | BGR         |
|                           | 2                |                        | YUV422² | 0              | YUYV        |
|                           | 3                |                        | RGB565  | 1              | UYVY        |
|                           |                  |                        | GRAY²   | 1              | BGR         |
|                           |                  |                        |        | N/A            | YYY         |
| 1                         | N/A              | 0                      | YUV444  | 0              | YUV         |
|                           |                  | 1                      | YUV420² | 1              | N/A         |
|                           |                  |                        |        |                | YYU/YYV³     |

---

¹ The image formats can be converted into other formats supported by the encoder via configuring register field JPEG_SAMPLE_SEL:
- 0: YUV444
- 1: YUV422
- 2: YUV420

² Image format conversion is limited:
- YUV422: can only remain unchanged or be downsampled to YUV420. Setting JPEG_SAMPLE_SEL to 0 has no effect.
- YUV420 or GRAY: will not be converted, regardless of the value of JPEG_SAMPLE_SEL.

³ The pixel arrangement alternates between rows: odd-numbered rows use the YYU pattern, and even-numbered rows use the YYY pattern.

---

### 35.5.1.3 Configurable Quantization Coefficient Table

ESP32-P4 JPEG encoder has implemented four 8 x 8 quantization coefficient tables in its hardware, which allows 64 software-configurable coefficient values per table.

The precision of each quantization table is configurable via JPEG_QNR_PRECISION:
- 0: low 8-bit effective
- 1: low 16-bit effective

The coefficient values for each table can be configured in FIFO mode or non-FIFO mode depending on the value of JPEG_QNR_FIFO_EN:
- 0: non-FIFO mode, in which each coefficient is written to a specific address
- 1: FIFO mode, in which all coefficients are written to the same address

Table 35.5-2. Position Number of Coefficients in a Quantization Coefficient Table (Example)

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| 8 | 9 | 10| 11| 12| 13| 14| 15|

...
```