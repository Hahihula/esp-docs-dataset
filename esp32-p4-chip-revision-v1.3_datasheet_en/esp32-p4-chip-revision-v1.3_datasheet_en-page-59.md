Title: Functional Description

Subtitle: External LCD interface:
- Body Text:
  - Bullet Points:
    - "8/16/24-bit parallel output modes"
    - "RGB, MOTO6800, and I8080 LCD formats"
    - "LCD data retrieved from internal memory or external memory via GDMA"

Subtitle: External camera (DVP image sensor) interface:
- Body Text:
  - Bullet Points:
    - "8/16-bit parallel input modes"
    - "Camera data stored in internal or external memory via GDMA"
    - "Interrupt support"

Subtitle: Pin Assignment
- Body Text:
  For CAM and LCD interfaces of the Camera-LCD controller, the pins used can be chosen from any GPIOs via the GPIO Matrix.

Subtitle: H264 Encoder (Section Title)
- Subsection Numbering: 4.2.1.5

Body Text for Section "H264 Encoder":
ESP32-P4 contains a baseline H264 encoder, which is used for real-time video sequence compression, significantly reducing the total amount of data while minimizing video quality loss.

Subtitle: Feature List
- Body Text:
  - Bullet Points (Feature List):
    - YUV420 progressive video with the maximum encoding performance of 1080p@30fps
    - I-frame and P-frame
    - GOP mode and dual-stream mode (in dual-stream mode, the total bandwidth of the two video image sequences to be encoded should not exceed 1080p@30fps)
    - Intra luma macroblock of 4 x 4 and 16 x 16 partitioning
    - All nine prediction modes for 4 x 4 partitioning and all four prediction modes for 16 x 16 partitioning of intra luma macroblock
    - All four prediction modes for intra chroma macroblock
    - All partition modes of inter prediction macroblock: 4 x 4, 4 x 8, 8 x 4, 8 x 8, 8 x 16, 16 x 8, and 16 x 16
    - Motion estimation with the precision of 1/2 and 1/4 pixel
    - Search range of inter prediction horizontal motion being [-29.75, +16.75], vertical search range being [-13.75, +13.75]
    - Enabling and disabling the deblocking filter
    - Context adaptive variable length coding (CAVLC)
    - P-skip macroblock
    - P slice supporting I macroblock
    - Decimate operation of luma and chroma component quantization results
    - Fixed QP and rate control at the macroblock level

Footer:
- Company Name: "Espressif Systems"
- Page Numbering: 59
- Document Title (partially visible): "ESP32-P4 Series Datasheet v0.6" 
- Link Texts: "Submit Documentation Feedback"

(Note: The image contains a watermark with the text "SAMPLE" diagonally across it.)