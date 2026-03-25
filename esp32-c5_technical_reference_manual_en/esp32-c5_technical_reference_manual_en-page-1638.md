

```markdown
- Variety of clock sources:
    - Including external IO clock PAD_CLK_TX/RX and internal system clocks XTAL_CLK, PLL_F240M_CLK, and RC_FAST_CLK
    - Maximum clock frequency of 40 MHz
    - Integer clock frequency division
- 1/2/4/8-bit configurable data bus width
- Full-duplex communication with 8-bit data bus width
- Bit reversal when data bus width is 1/2/4-bit
- RX unit for receiving IO parallel data, which supports:
    - Output clock gating
    - RX unit input and output clock inverse
    - Various receive modes
    - Configurable GDMA SUC EOF generation
    - Configurable IO pin of external enable signal
- TX unit for sending IO parallel data, which supports:
    - Chip select function
    - Output clock gating
    - TX unit input and output clock inverse
    - Configurable bus idle value
```