

```markdown
Chapter 35  JPEG Codec



GoBack


35.7.3    Reset

Users can reset JPEG codec entirely or partially, depending on the actual scenarios, at any time during the encoding or decoding process:

*   The entire JPEG codec, including all the RAMs and FIFOs as well as all the state machines: set JPEG_SOFT_RST to 1. In this case, the register configuration value will not be reset.
*   Only all the RAMs and FIFOs inside the JPEG codec, for example, changing the quantization coefficient tables or Huffman tables: set JPEG_FIFO_RST to 1.
*   Only all the state machines inside the JPEG codec, for example, only stop the current encoding or decoding process: set JPEG_FSM_RST to 1.
```