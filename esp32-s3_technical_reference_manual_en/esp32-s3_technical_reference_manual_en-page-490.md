**Table:**

| Signal No. | Input Signal | Default value | Direct Input via IO MUX | Output Signal | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|--------------|---------------|-------------------------|---------------|---------------------------------------------|----------------------------|
| 186        | sdhost_cdata_in_16 | - | no | sdhost_cdata_out_16 | sdhost_cdata_out_en_16 | no |
| 187        | sdhost_cdata_in_17 | - | no | sdhost_cdata_out_17 | sdhost_cdata_out_en_17 | no |
| 188        | -             | -             | -                        | -              | 1'd1                                        | -                          |
| 189        | -             | -             | -                        | -              | 1'd1                                        | -                          |
| 190        | -             | -             | -                        | -              | 1'd1                                        | -                          |
| 191        | -             | -             | -                        | -              | 1'd1                                        | -                          |
| 192        | sdhost_data_strobe_1 | 0   | no | -               | 1'd1                                      | -                          |
| 193        | sdhost_data_strobe_2 | 0   | no | -               | 1'd1                                      | -                          |
| 194        | sdhost_card_detect_n_1 | 0   | no | -               | 1'd1                                      | -                          |
| 195        | sdhost_card_detect_n_2 | 0   | no | -               | 1'd1                                      | -                          |
| 196        | sdhost_card_write_prt_1 | 0   | no | -               | 1'd1                                      | -                          |
| 197        | sdhost_card_write_prt_2 | 0   | no | -               | 1'd1                                      | -                          |
| 198        | sdhost_card_int_n_1 | 0   | no | -               | 1'd1                                      | -                          |
| 199        | sdhost_card_int_n_2 | 0   | no | -               | 1'd1                                      | -                          |
| 200        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 201        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 202        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 203        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 204        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 205        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 206        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 207        | -             | -             | -                        | -              | 1'd1                                        | no                         |
| 208        | sig_in_func_208 | O   | no | sig_in_func208    | 1'd1                                      | no                          |
| 209        | sig_in_func_209 | O   | no | sig_in_func209    | 1'd1                                      | no                          |
| 210        | sig_in_func_210 | -             | -                        | sig_in_func210 | 1'd1                                      | no                          |
| 211        | sig_in_func_211 | O   | no | sig_in_func211    | 1'd1                                      | no                          |
| 212        | sig_in_func_212 | -             | -                        | sig_in_func212 | 1'd1                                      | no                          |

**Footer:**

- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback
- GoBack