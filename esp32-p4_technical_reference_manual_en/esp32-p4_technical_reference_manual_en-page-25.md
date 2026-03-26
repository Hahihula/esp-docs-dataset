

```markdown
35.2 Introduction 1594
35.3 Features 1595
35.4 Architectural Overview 1596
35.5 Functional Description 1597
    35.5.1 JPEG Encoder 1598
        35.5.1.1 Pause 1598
        35.5.1.2 Color Space Conversion 1598
        35.5.1.3 Configurable Quantization Coefficient Table 1599
        35.5.1.4 Stuffed Zero Byte 1601
        35.5.1.5 EOI Marker 1601
    35.5.2 JPEG Decoder 1601
        35.5.2.1 Multiple Chrominance Components 1601
        35.5.2.2 Parsing RST Marker 1602
        35.5.2.3 Configurable Quantization Coefficient Table 1603
        35.5.2.4 Configurable Huffman Table 1603
        35.5.2.5 Timeout Detection 1605
35.6 Interrupts 1605
35.7 Programming Procedures 1607
    35.7.1 JPEG Encoder 1607
    35.7.2 JPEG Decoder 1610
    35.7.3 Reset 1614
35.8 Register Summary 1615
35.9 Registers 1616

36 Image Signal Processor (ISP) 1638
36.1 Introduction 1638
36.2 Terminology 1639
36.3 Feature List 1639
36.4 Architectural Overview 1640
36.5 Functional Description 1640
    36.5.1 ISP_Header 1640
    36.5.2 ISP_Pipeline 1641
        36.5.2.1 Black Level Correction (BLC) 1641
        36.5.2.2 Defective Pixel Correction (DPC) 1641
        36.5.2.3 Bayer Filter (BF) 1642
        36.5.2.4 Lens Shading Correction (LSC) 1642
        36.5.2.5 Demosaic 1643
        36.5.2.6 White Balance Gain (WBG) 1643
        36.5.2.7 Color Correction Matrix (CCM) 1644
        36.5.2.8 Gamma Correction 1644
        36.5.2.9 RGB2YUV 1645
        36.5.2.10 Sharpen 1645
        36.5.2.11 Contrast/Hue/Saturation/Luminance Adjustment (COLOR) 1645
        36.5.2.12 YUV_Limit and YUV2RGB 1646
        36.5.2.13 Cropping (CROP) 1646
        36.5.2.14 Automatic Exposure Statistics (AE) 1646
```