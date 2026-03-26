

```markdown
Chapter 25 AES Accelerator (AES)

The length of source data for AES accelerator under DMA-AES working mode must be 128 bits or the integral multiples of 128 bits. Otherwise, trailing zeros will be added to the original source data, so the length of source data equals to the nearest integral multiples of 128 bits. Please see details in Table 25.6-3 below.

Table 25.6-3. TEXT-PADDING

Function: TEXT-PADDING()
Input : X, bit string.
Output : Y = TEXT-PADDING(X), whose length is the nearest integral multiples of 128 bits.

Steps
Let us assume that X is a data-stream that can be split into n parts as following:
X = X₁||X₂||⋯||X_{n-1}||X_n
Here, the lengths of X₁,X₂,⋯,X_{n-1} all equal to 128 bits, and the length of X_n is t (0<=t<=127).
If t = 0, then
TEXT-PADDING(X) = X;
If 0 < t <= 127, define a 128-bit block, X*_n^*, and let X*_n^* = X_n ||(0)^{128-t}, then
TEXT-PADDING(X) = X₁||X₂||⋯||X_{n-1}||X*_n^* = X ||(0)^{128-t}

25.6.2 Endianness

Under the DMA-AES working mode, the transmission of source data and result data for AES accelerator is solely controlled by DMA. Therefore, the AES accelerator cannot control the Endianness of the source data and result data, but does have requirement on how these data should be stored in memory and on the length of the data.

For example, let us assume DMA needs to write the following data into memory at address 0x0280.
• Data represented in hexadecimal:
    - 010203040506070809A0B0C0D0EOF101112131415161718191A1B1C1D1E1F20
• Data Length:
    - Equals to 2 blocks.

Then, this data will be stored in memory as shown in Table 25.6-4 below.

Table 25.6-4. Text Endianness for DMA-AES

| Address | Byte | Address | Byte | Address | Byte | Address | Byte |
|---------|------|---------|------|---------|------|---------|------|
| 0x0280  | 0x01 | 0x0281  | 0x02 | 0x0282  | 0x03 | 0x0283  | 0x04 |
| 0x0284  | 0x05 | 0x0285  | 0x06 | 0x0286  | 0x07 | 0x0287  | 0x08 |
| 0x0288  | 0x09 | 0x0289  | 0x0A | 0x028A  | 0x0B | 0x028B  | 0x0C |
| 0x028C  | 0x0D | 0x028D  | 0x0E | 0x028E  | 0x0F | 0x028F  | 0x10 |
| 0x0290  | 0x11 | 0x0291  | 0x12 | 0x0292  | 0x13 | 0x0293  | 0x14 |
| 0x0294  | 0x15 | 0x0295  | 0x16 | 0x0296  | 0x17 | 0x0297  | 0x18 |
| 0x0298  | 0x19 | 0x0299  | 0x1A | 0x029A  | 0x1B | 0x029B  | 0x1C |
| 0x029C  | 0x1D | 0x029D  | 0x1E | 0x029E  | 0x1F | 0x029F  | 0x20 |

Espressif Systems
```