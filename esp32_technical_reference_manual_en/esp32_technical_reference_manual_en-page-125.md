**Table:**

| Signal No. | Input Signals | Default Value If Unassigned* | Same Input Signal from IO_MUX Core | Output Signals | Output Enable of Output Signals |
|------------|---------------|-------------------------------|-------------------------------------|----------------|---------------------------------|
| 6          | SPICS1_in     | O                             | no                                  | SPICS1_out    | SPICS1_oe                        |
| 7          | SPICS2_in     | O                             | no                                  | SPICS2_out    | SPICS2_oe                        |
| 8          | HSPICLK_in    | yes                          |                                     | HSPICLK_out   | HSPICLK_oe                       |
| 9          | HSPIQ_in      | O                             | yes                                 | HSPIQ_out     | HSPIQ_oe                         |
| 10         | HSPID_in      | yes                          |                                     | HSPID_out     | HSPID_oe                         |
| 11         | HSPIOCS0_in   | O                             | yes                                 | HSPIOCS0_out  | HSPIOCS0_oe                      |
| 12         | HSPIHD_in     | O                             | yes                                 | HSPIHD_out    | HSPIHD_oe                        |
| 13         | HSPIWP_in     | O                             | yes                                 | HSPIWP_out    | HSPIWP_oe                        |
| 14         | U0RXD_in      | yes                          |                                     | U0TXD_out     | 'd1'                            |
| 15         | UOCTS_in      | yes                          |                                     | UORTS_out     | 'd1'                            |
| 16         | UODSR_in      | no                           |                                     | UODTR_out     | 'd1'                            |
| 17         | U1RXD_in      | yes                          |                                     | U1TXD_out     | 'd1'                            |
| 18         | U1CTS_in      | yes                          |                                     | U1RTS_out     | 'd1'                            |
| 23         | I2SO0_BCK_in  | O                             | no                                  | I2SO0_BCK_out | 'd1'                            |
| 24         | I2S10_BCK_in  | O                             |                                     | I2S10_BCK_out | 'd1'                            |
| 25         | I2SO0_WS_in   | O                             | no                                  | I2SO0_WS_out  | 'd1'                            |
| 26         | I2S10_WS_in   | O                             |                                     | I2S10_WS_out  | 'd1'                            |
| 27         | I2SO1_BCK_in  | O                             | no                                  | I2SO1_BCK_out | 'd1'                            |
| 28         | I2SO1_WS_in   | O                             |                                     | I2SO1_WS_out  | 'd1'                            |
| 29         | I2CEXTO_SCL_in| 1                            | no                                  | I2CEXTO_SCL_out| 'd1'                            |
| 30         | I2CEXTO_SDA_in| 1                            |                                     | I2CEXTO_SDA_out| 'd1'                            |
| 31         | pwm0_sync0_in | O                             | no                                  | sdio_tohost_int_out| 'd1' |
| 32         | pwm0_sync1_in | O                             |                                     | pwm0_out0a    | 'd1'                            |
| 33         | pwm0_sync2_in | O                             |                                     | pwm0_out0b    | 'd1'                            |
| 34         | pwm0_f0_in    | O                             | no                                  | pwm0_out1a    | 'd1'                            |
| 35         | pwm0_f1_in    | O                             |                                     | pwm0_out1b    | 'd1'                            |

**Footer:**
- ESP32 TRM (Version 5.6)
- Submit Documentation Feedback
- GoBack

**Side Texts:** 
- "Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)"
- "Espressif Systems"