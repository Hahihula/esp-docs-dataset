

```markdown
| AES_STATE_REG[1:0] | Status | Description |
|--------------------|--------|-------------|
| 0                  | IDLE   | The AES accelerator is idle. |
| 1                  | WORK   | The AES accelerator is in the middle of an operation. |
| 2                  | DONE   | The AES accelerator completed operations. |

Table 19.6-2. Working Status under DMA-AES Working mode

Function: TEXT-PADDING()
Input    : X, bit string.
Output   : Y = TEXT-PADDING(X), whose length is the nearest integral multiples of 128 bits.

Steps
Let us assume that X is a data-stream that can be split into n parts as following:
X = X₁||X₂||⋯||X_{n−1}||Xₙ
Here, the lengths of X₁,X₂,⋯,X_{n−1} all equal to 128 bits, and the length of Xₙ is t (0<=t<=127).
If t = 0, then
TEXT-PADDING(X) = X;
If 0 < t <= 127, define a 128-bit block, X*_n*, and let X*_n* = Xₙ||0^{128−t}, then
TEXT-PADDING(X) = X₁||X₂||⋯||X_{n−1}||X*_n* = X||0^{128−t}
```