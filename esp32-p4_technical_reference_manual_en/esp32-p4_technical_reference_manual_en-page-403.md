

```markdown
| Bits | Name                  | Description |
|------|-----------------------|-------------|
|      |                       | Address of the next descriptor. If the current descriptor is the last descriptor in the linked list, this value can be 0. This address can point to the address space of internal or external memory. |
| DW4  | Next descriptor address | Note: The starting address for storing 2D-DMA descriptors must be 8-byte aligned. |

## 6.4.3 Padding in 2D-MOD1 Mode and DSCR-PORT Mode

This section only applies to the TX direction of 2D-DMA transfers in 2D-MOD1 and DSCR-PORT mode.

For JPEG decoding, the basic unit of image data input is a block of 8 × 8, 8 × 16, or 16 × 16 (pixels). In 2D-MOD1 mode, when the length and width of the image are not integer multiples of the basic unit, the image needs to pad out to integer multiples of the basic unit based on the previous or the current macroblock.

For PPA, the basic unit for transmit channels in DSCR-PORT mode is 36 × 36 (YUV420), 36 × 34 (YUV422) and 34 × 34 (horizontal × vertical). The width and height of a basic unit for different transmit channels are configured using DMA2D_OUT_DSCR_PORT_BLK_H_CHn and DMA2D_OUT_DSCR_PORT_BLK_V_CHn. When the length and width of the image are not integer multiples of the basic unit, the image needs to pad out.

Below are the padding rules:

* Horizontally, the padding depends on the pbyte field of DW1.
  - When pbyte is 0 (0.5 byte/pixel), the remaining pixels must be even, and the padding is the last 0.5 byte.
  - When pbyte is 1 (1 byte/pixel), the padding is the last 1 byte.
  - When pbyte is 2 (1.5 bytes/pixel), the remaining pixels must be even, and the padding is the last 3 bytes.
  - When pbyte is 3 (2 bytes/pixel), the padding is the last 2 bytes.
  - When pbyte is 4 (3 bytes/pixel), the padding is the last 3 bytes.
  - When pbyte is 5 (4 bytes/pixel), the padding is the last 4 bytes.
* Vertically, the padding is the last row.

Figure 6.4-2 and Figure 6.4-3 illustrate the padding method.

In Figure 6.4-2, a blue grid represents a basic unit (a block of 8 × 8, 8 × 16, or 16 × 16 pixels), and a yellow box (incomplete basic unit) along with a green box (padding) forms a basic unit.

In Figure 6.4-3, a grid represents one pixel, and the numbers inside each grid represent pixel values.
```