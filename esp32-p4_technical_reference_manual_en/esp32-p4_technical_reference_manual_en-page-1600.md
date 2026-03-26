

```markdown
|56|57|58|59|60|61|62|63|
|:----|:----|:----|:----|:----|:----|:----|:----|
```

In different modes, the configuration of the quantization coefficient table is different. Note, n (n = 0, 1, 2, 3) indicates the number of each quantization coefficient table:

*   non-FIFO mode: each quantization coefficient in a specific position of a quantization coefficient table n must be written to a specific address, which is (JPEG codec base address + n * 0x100 + quantization coefficient position number * 0x4), in which the quantization coefficient position number can be 0, 1, 2, ..., 63 (see Table 35.5-2). In this mode, since each coefficient is written to a specific address, configuring the 64 quantization coefficients in sequence is not required.
*   FIFO mode: all 64 quantization coefficients of the quantization table n are written to the same address, which is JPEG_TnQNR_REG. In this mode, since all coefficients are written to the same address, configuring the 64 quantization coefficients one by one in sequence is required. Afterwards, the hardware will automatically store these 64 quantization coefficients in sequence as shown in Table 35.5-2.

If there are less than 4 quantization tables, the corresponding quantization table will not be written.

To use a specific quantization coefficient table n for the luminance component or the chrominance component, just set the corresponding register fields to n:

*   luminance component: JPEG_LQNR_TBL_SEL
*   chrominance component: JPEG_CQNR_TBL_SEL

The JPEG baseline standard recommended 8-bit precision quantization coefficient tables for the luminance component and the chrominance component are shown in Table 35.5-3 and Table 35.5-4.

Table 35.5-3. Recommended 8-bit Precision Quantization Coefficient Table for the Luminance Component

|16|11|10|16|24|40|51|61|
|:----|:----|:----|:----|:----|:----|:----|:----|
|12|  |  |19|26|58|60|55|
|14|13|16|24|40|57|69|56|
|  |17|22|29|51|87|80|62|
|18|22|37|56|68|109|103|77|
|24|35|55|64|81|104|113|92|
|49|64|78|87|103|121|120|101|
|72|92|95|98|112|100|103|99|

Table 35.5-4. Recommended 8-bit Precision Quantization Coefficient Table for the Chrominance Component

|17|18|24|47|99|99|99|99|
|:----|:----|:----|:----|:----|:----|:----|:----|
|  |21|26|66|99|99|99|99|
|24|26|56|99|99|99|99|99|
|47|66|99|99|99|99|99|99|
|99|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
```