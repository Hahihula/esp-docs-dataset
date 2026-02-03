**Table:**

| Signal No | Input Signal       | Default value | Direct Input via IO MUX | Output Signal         | Output enable signal when GPIO FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|-----------|--------------------|---------------|-------------------------|-----------------------|--------------------------------------------------|----------------------------|
| 133       | CAM_DATA_in0       | O             | no                      | LCD_DATA_out0        | 1'd1                                             | no                          |
| 134       | CAM_DATA_in1       | O             | no                      | LCD_DATA_out1        | 1'd1                                             | no                          |
| 135       | CAM_DATA_in2       | O             | no                      | LCD_DATA_out2        | 1'd1                                             | no                          |
| 136       | CAM_DATA_in3       | O             | no                      | LCD_DATA_out3        | 1'd1                                             | no                          |
| 137       | CAM_DATA_in4       | O             | no                      | LCD_DATA_out4        | 1'd1                                             | no                          |
| 138       | CAM_DATA_in5       | O             | no                      | LCD_DATA_out5        | 1'd1                                             | no                          |
| 139       | CAM_DATA_in6       | O             | no                      | LCD_DATA_out6        | 1'd1                                             | no                          |
| 140       | CAM_DATA_in7       | O             | no                      | LCD_DATA_out7        | 1'd1                                             | no                          |
| 141       | CAM_DATA_in8       | O             | no                      | LCD_DATA_out8        | 1'd1                                             | no                          |
| 142       | CAM_DATA_in9       | O             | no                      | LCD_DATA_out9        | 1'd1                                             | no                          |
| 143       | CAM_DATA_in10      | O             | no                      | LCD_DATA_out10       | 1'd1                                             | no                          |
| 144       | CAM_DATA_in11      | O             | no                      | LCD_DATA_out11       | 1'd1                                             | no                          |
| 145       | CAM_DATA_in12      | O             | no                      | LCD_DATA_out12       | 1'd1                                             | no                          |
| 146       | CAM_DATA_in13      | O             | no                      | LCD_DATA_out13       | 1'd1                                             | no                          |
| 147       | CAM_DATA_in14      | O             | no                      | LCD_DATA_out14       | 1'd1                                             | no                          |
| 148       | CAM_DATA_in15      | O             | no                      | LCD_DATA_out15       | 1'd1                                             | no                          |
| 149       | CAM_PCLK          | -             | -                       | CAM_CLK              | -                                               | -                           |
| 150       | CAM_H_ENABLE       | -             | -                       | LCD_H_ENABLE         | -                                               | -                           |
| 151       | CAM_H_SYNC         | O             | no                      | LCD_H_SYNC           | 1'd1                                             | no                          |
| 152       | CAM_V_SYNC         | O             | no                      | LCD_V_SYNC           | 1'd1                                             | no                          |
| 153       | -                  | -             | -                       | LCD_DC               | -                                               | -                           |
| 154       | -                  | -             | -                       | LCD_PCLK            | 1'd1                                             | no                          |
| 155       | SUBSPID4_in        | O             | yes                     | SUBSPID4_out         | SUBSPID4_oe                                     | no                          |
| 156       | SUBSPID5_in        | -             | -                       | SUBSPID5_out         | SUBSPID5_oe                                     | no                          |
| 157       | SUBSPID6_in        | O             | yes                     | SUBSPID6_out         | SUBSPID6_oe                                     | no                          |
| 158       | SUBSPID7_in        | -             | -                       | SUBSPID7_out         | SUBSPID7_oe                                     | no                          |
| 159       | SUBSPIDQS_in       | O             | yes                     | SUBSPIDQs_out        | SUBSPIDQs_oe                                    | no                          |

**Side Text:**
- "Espressif Systems"
- "Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)"
- "Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)"

**Footer:**
- Page number indicator ("488")
- Navigation link or button labeled "GoBack"