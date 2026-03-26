

```markdown
example, {B3, B2, B1, B0} represents a 32-bit data, wherein BO represents bit 0-7, B1 represents bit 8-15, B2 represents bit 16-23, and B3 represents bit 24-31.

## 46.9.1.3 A-law/μ-law Compression and Decompression

ESP32-P4 I2Sn compresses/decompresses the valid data into 32-bit by A-law or by μ-law. If the bit width of valid data is smaller than 32, zeros are filled to the extra high bits of the data to be compressed/decompressed by default.

**Note:**
Extra high bits here mean the bits[31: channel valid data width] of the data to be compressed/decompressed.

Configure I2S_TX_PCM_BYPASS:
- 0: Compress or decompress the data
- 1: Do not compress or decompress the data

Configure I2S_TX_PCM_CONF:
- 0: Decompress the data using A-law
- 1: Compress the data using A-law
- 2: Decompress the data using μ-law
- 3: Compress the data using μ-law

At this point, the first phase of data format control is completed.

## 46.9.1.4 Bit Width Control of Channel TX Data

The TX data width in each channel is determined by I2S_TX_TDM_CHAN_BITS.

* If TX data width in each channel is larger than the valid data width, zeros will be filled to these extra bits.
Configure I2S_TX_LEFT_ALIGN:
- 0: The valid data is at the lower bits of TX data. Zeros are filled into higher bits of TX data;
- 1: The valid data is at the higher bits of TX data. Zeros are filled into lower bits of TX data.

* If the TX data width in each channel is smaller than the valid data width, only the lower bits of valid data are sent out, and the higher bits are discarded.

At this point, the second phase of data format control is completed.

## 46.9.1.5 Bit Order Control of Channel Data

The data bit order in each channel is controlled by I2S_TX_BIT_ORDER:

- 0: Not reverse the valid data bit order;
- 1: Reverse the valid data bit order.

At this point, the data format control is completed. The data after format control will be sent sequentially from high to low. Figure 46.9-1 shows the complete process of TX data format control.
```