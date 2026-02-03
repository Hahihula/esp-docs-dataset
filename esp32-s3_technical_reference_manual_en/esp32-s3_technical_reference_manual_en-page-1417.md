**Chapter Title:**
Remote Control Peripheral (RMT)

**Section Header:**
37.3.2.1 RAM Architecture

**Body Text:**
Figure **37.3-2** shows the format of pulse code in RAM. Each pulse code contains a 16-bit entry with two fields: “level” and “period”. The field "level" (0 or 1) indicates whether it is low/high-level value was received, while“period” points out the number of clock cycles.

**Figure Caption:** 
Format of Pulse Code in RAM

**Equation Description:**
The minimum value for the period is zero (0) and interpreted as a transmission end-marker. For non-zero period (i.e., not an end-marker), its value limited by APB clock and RMT clock according to equation below:

\[ 3 \times T_{apb\_clk} + 5 \times T_{rmt\_clk} < period \times T_{clk\_div} \]

**Note:**
According to the above, frequency of rmt_sclk, pulse width (i.e., period × \(T_{clk\_div}\)) able to be captured by RMT is limited as follows:
- The minimum value of pulse width should larger than (\(3 \times T_{apb\_clk} + 5 \times T_{rmt\_clk}\)).
- the maximum value of pulse width should smaller or equal (the maximum period × \(T_{clk\_div}\)), i.e., ((\(2^{15}-1\) × the maximum \(T_{rmt\_clk} \times 256\)).

For more information about rmt_sclk frequency, APB_CLK frequency, see Section **37.3.3** or Chapter *7 Reset and Clock*.

**Subsection Header:**
37.3.2.2 Use of RAM

**Body Text:**
The RAM is divided into eight 48 x 32-bit blocks. By default, each channel uses one block (block O for channel 0, block I for channel 1).

If the data size of single transfer larger than one block size TX channel \(n\) or RX channel \(m\), users can configure:
- to enable wrap mode by setting RMT_MEM_TX/RX.WRAP_EN\_CHn/m.
- use more blocks by configuring RMT_MEM_SIZE_CHn/m.

Setting **RMT_MEM_SIZE_CHn/m > 1** allows the memory of subsequent channels, block (n/m) ~ block (\(n + MRT_MEM_SIZE_CHn/m - 1\)). If so, then the subsequent channels \(n/m + 1\) ~ \(n/m + RMT_MEM_SIZE_CHn/m - 1\) can not be used once their RAM blocks are occupied. For example, if channel O is configured to use more than one block.

**Footer:**
Espressif Systems
Page number (bottom center): 1417

**Link:** 
ESP32-S3 TRM (Version *1.7*)

**Action Button:**
Submit Documentation Feedback