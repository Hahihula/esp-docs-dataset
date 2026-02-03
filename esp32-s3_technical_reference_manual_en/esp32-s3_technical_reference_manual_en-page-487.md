**Table:**

| Signal No. | Input Signal       | Default value | Direct Input via IO MUX | Output Signal    | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|------------|--------------------|---------------|-------------------------|------------------|-------------------------------------------------|----------------------------|
| 106        | FSPII04_in         | O             | yes                     | FSPII04_out      | FSPII04_oe                                      | yes                         |
| 107        | FSPII05_in         | O             | yes                     | FSPII05_out      | FSPII05_oe                                      | yes                         |
| 108        | FSPII06_in         | O             | yes                     | FSPII06_out      | FSPII06_oe                                      | yes                         |
| 109        | FSPII07_in         | O             | yes                     | FSPII07_out      | FSPII07_oe                                      | yes                         |
| 110        | FSPIO0_in          | O             | yes                     | FSPIO0_out       | FSPIO0_oe                                      | yes                         |
| 111        | -                  | -             | -                       | FSPIO1_out       | FSPIO1_oe                                      | no                          |
| 112        | -                  | -             | -                       | FSPIO2_out       | FSPIO2_oe                                      | no                          |
| 113        | -                  | -             | -                       | FSPIO3_out       | FSPIO3_oe                                      | no                          |
| 114        | -                  | -             | -                       | FSPIO4_out       | FSPIO4_oe                                      | no                          |
| 115        | -                  | -             | -                       | FSPIO5_out       | FSPIO5_oe                                      | no                          |
| 116        | twai_rx            | 1             | no                      | twai_tx          | '1'd                                            | no                          |
| 117        | -                  | -             | -                       | twai_bus_off_on  | '1'd                                            | no                          |
| 118        | -                  | -             | -                       | twai_clkout      | '1'd                                            | no                          |
| 119        | -                  | -             | -                       | SUBSPICLK_out_mux| SUBSPICLK_oe                                    | no                          |
| 120        | SUBSPIQ_in         | O             | yes                     | SUBSPIQ_out      | SUBSPIQ_oe                                      | yes                         |
| 121        | SUBSPID_in         | O             | yes                     | SUBSPID_out      | SUBPID_oe                                       | yes                         |
| 122        | SUBSPIHD_in        | O             | yes                     | SUBSPIHD_out     | SUBPIHD_oe                                      | yes                         |
| 123        | SUBSPIWP_in        | O             | yes                     | SUBSPIWP_out     | SUBPIWP_oe                                      | yes                         |
| 124        | -                  | -             | -                       | SUBSPICS0_out    | SUBSPICS0_oe                                    | yes                         |
| 125        | -                  | -             | -                       | SUBSPICS1_out    | SUBSPICS1_oe                                    | yes                         |
| 126        | -                  | -             | -                       | FSPIQDS_out      | FSPIQDS_oe                                      | yes                         |
| 127        | -                  | -             | -                       | SPI3_CS2_out     | SPI3_CS2_oe                                     | no                          |
| 128        | -                  | -             | -                       | I2S00_SD1_out    | '1'd                                            | no                          |
| 129        | Core1_gpio_in0    | O             | no                      | Core1_gpio_out0  | '1'd                                            | no                          |
| 130        | Core1_gpio_in1    | O             | no                      | Core1_gpio_out1  | '1'd                                            | no                          |
| 131        | Core1_gpio_in2    | O             | no                      | Core1_gpio_out2  | '1'd                                            | no                          |
| 132        | -                  | -             | -                       | LCD_CS           | '1'd                                            | no                          |

**Footer:**
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback
- GoBack