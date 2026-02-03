**Title: Chapter 5 eFuse Controller**

---

### Figure Caption

- **Figure 5.3-1:** Shift Register Circuit (output of first 32 bytes)
- **Figure 5.3-2:** Shift Register Circuit (output of last 12 bytes)

---

#### Text Content:

- Bytes [0:31] are the data bytes itself
- Bytes [32:43] are the encoded parity bytes stored in 8-bit flip-flops DFF1, DFF2,..., DFF12 (gf_mul_n, where n is an integer, is the result of multiplying a byte of data ...)

After that, the hardware burns into eFuse the 44-byte codeword consisting of the data bytes followed by the parity bytes.

When the eFuse block is read back, the eFuse controller automatically decodes the codeword and applies error correction if needed.
Because the RS check codes are generated on the entire 256-bit eFuse block, each block can only be written once.

---

#### Subtitle: Programming of Parameters

The eFuse controller can only program eFuse parameters of one block at a time. BLOCK0 ~ BLOCK10 share the same address range to store the parameters to be programmed. Configure parameter EFUSE_BLK_NUM to indicate which block should be programmed.
Before programming, make sure the eFuse programming voltage VDDQ is configured correctly as described in Section 5.3.4.

---

#### Programming Block

Espressif Systems  
Submit Documentation Feedback  

ESP32-S3 TRM (Version 1.7)