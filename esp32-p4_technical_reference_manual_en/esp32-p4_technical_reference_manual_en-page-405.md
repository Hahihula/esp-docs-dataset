

```markdown
## Table 6.4-2. Selecting Peripherals via Register Configuration in TX Direction

| DMA2D_PERI_OUT_SEL_CHn | Peripheral                |
|-------------------------|----------------------------|
| 0                       | JPEG                      |
| 1                       | PPA's SRM module           |
| 2                       | PPA's BLEND0 module        |
| 3                       | PPA's BLEND1 module        |
| 4 ~ 7                   | Dummy-4 ~ 7                |

## Table 6.4-3. Selecting Peripherals via Register Configuration in RX Direction

| DMA2D_PERI_IN_SEL_CHn | Peripheral                |
|------------------------|----------------------------|
| 0                      | JPEG                      |
| 1                      | PPA's SRM module           |
| 2                      | PPA's BLEND channel        |
| 3 ~ 7                  | Dummy-3 ~ 7                |

## 6.4.5 Memory-to-Memory Data Transfer

The 2D-DMA controller allows memory-to-memory data transfer only in 1D mode and 2D-MODO mode. Such data transfer can be enabled by setting `DMA2D_IN_MEM_TRANS_EN_CHn`, which connects the output of transmit channel `n` to the input of receive channel `n`. Note that a transmit channel can only be connected to the receive channel with the same number (`n`), and `DMA2D_IN_PERI_SEL_CHn` and `DMA2D_OUT_PERI_SEL_CHn` should be configured to any value corresponding to "Dummy".

Memory-to-memory data transfer can be used in combination with color space conversion so that a macroblock can be moved from one segment of memory address space to another with its color space converted.

## 6.4.6 Macroblock Reordering

### 6.4.6.1 Macroblock Reordering in TX Direction

When the 2D-DMA accesses external memory via SPI, in order to improve the bandwidth utilization of SPI, it is necessary to initiate AXI transfers with a larger burst length. In 2D-MOD1 mode, the 2D-DMA can increase the burst length of AXI transfers by fetching multiple macroblocks at once. For example, the 2D-DMA can fetch five macroblocks of 8x8 pixels in one operation, and in this case, the hb field in the descriptor should be 40 and vb should be 8. However, the JPEG requires the 2D-DMA to send data in the order of macroblocks. This means that the 2D-DMA needs to reorder the fetched macroblocks to meet the requirements of JPEG.

Recommended configurations for macroblock reordering are listed in Table 6.4-4.
```