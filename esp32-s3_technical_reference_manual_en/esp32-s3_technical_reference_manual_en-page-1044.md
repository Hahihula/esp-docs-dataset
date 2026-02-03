**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Titles and Content:**

1. **28.5.3 TDM PCM Standard**
   - Short frame synchronization under PCM standard requires WS signal changes one BCK clock cycle earlier than SD signal on the falling edge of BCK, which means that the WS signal becomes valid one clock cycle before transferring the first bit of channel data and remains unchanged in this BCK clock cycle.
   - TDM PCM standard supports multiple channels. 
   - Compared with PCM standard.

2. **Figure 28.5-3:**
   - Title: "TDM PCM Standard Timing Diagram"
   - Description: Illustrates the timing diagram for a single channel under TDM PCM standards, showing WS(LRCK), BCK(SCLK), and SD(SDOUT) signals with multiple channels (Channel 0 to Channel n+1).

3. **28.5.4 PDM Standard**
   - Under PDM standard, WS signal changes continuously during data transmission.
   - The low-level and high-level of this signal indicates the left channel and right channel respectively.

4. **Figure 28.5-4:**
   - Title: "PDM Standard Timing Diagram"
   - Description: Illustrates a timing diagram for PDM standards, showing WS(LRCK), BCK(SCLK), SD(SDOUT) signals with data transmission on the falling edge of BCK.

**Section Titles and Content Continued:**

1. **28.6 TX/RX Clock**
   - I2S_n_TX/RX_CLK as shown in Figure 28.6-1 is the master clock of I2S_n TX/RX unit, divided from:
     - Espressif Systems
     - ESP32-S3 TRM (Version 1.7)

**Footer:**
- Page number and document version information.
- "Submit Documentation Feedback" link.

**Diagrams in Markdown format with descriptions as provided above:** 

```markdown
### Figure 28.5-3:
Title: TDM PCM Standard Timing Diagram

WS(LRCK) | BCK(SCLK) | SD(SDOUT)
|---|---|---
| WS signal change earlier than SD on falling edge of BCK cycle.
| WS becomes valid one clock cycle before transferring the first bit.

### Figure 28.5-4:
Title: PDM Standard Timing Diagram

WS(LRCK) | BCK(SCLK) | SD(SDOUT)
|---|---|---
| Continuous changes during data transmission, indicating left and right channels.
```