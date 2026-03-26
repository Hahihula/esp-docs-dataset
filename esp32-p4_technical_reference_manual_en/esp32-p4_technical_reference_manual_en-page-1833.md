

```markdown
Chapter 39  
H264 Encoder  

39.1 Overview  

The H264 encoder is based on the H264 standard. It is used for real-time compression of video sequences, which can significantly reduce the total amount of data with minimal loss of video quality.  

39.2 Terminology  

| Term          | Definition                                                                                     |
|---------------|-----------------------------------------------------------------------------------------------|
| bitstream     | A sequence of bits that forms the representation of one or more coded video sequences.         |
| profile       | A subset of the entire bitstream syntax that is specified by the H264 standard.                |
| level         | Specified within each profile. A specified set constrains imposed on values of the syntax elements in the bitstream. |
| MB            | The full name is macroblock. It is a 16 x 16 block of luma samples and two corresponding blocks of chroma samples of a picture that has three sample arrays. |
| slice         | An integer number of MBs.                                                                     |
| I frame       | Intra frame.                                                                                |
| P frame       | Inter frame.                                                                                 |
| I slice       | Slice in I frame.                                                                            |
| P slice       | Slice in P frame.                                                                            |
| P-skip MBs    | MBs in P frame that skip the encoding.                                                      |
| CAVLC         | Context-based adaptive variable length coding.                                               |
| MV            | Motion vector.                                                                               |
| GOP           | Group of pictures. In a GOP, the first frame is an I frame, and subsequent frames are P frames. |
| QP            | Quantization parameter.                                                                      |
| ROI           | Region of interest.                                                                          |
| AXI           | Advanced extensible interface.                                                              |
| TX            | Transmit.                                                                                   |
| RX            | Receive.                                                                                    |
| DB            | Deblocking filter.                                                                           |
| NUM_H_MB      | Number of horizontal MBs in a picture.                                                      |

39.3 Features  

The H264 encoder supports the following features:
```