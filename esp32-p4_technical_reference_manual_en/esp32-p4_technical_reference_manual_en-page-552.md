

```markdown
| Signal No. | Input Signal                  | Default Value | Direct Input via HP IO MUX | Output Signal                     | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|-------------------------------|---------------|-----------------------------|------------------------------------|----------------------------------------------|------------------------------|
| 0          | -                             | -             | -                           | sd_card_cclk_2_pad_out            | 'd1                                          | no                           |
| 1          | sd_card_ccmd_2_pad_in         | 1             | no                          | sd_card_ccmd_2_pad_out            | sd_card_ccmd_2_pad_oe                        | no                           |
| 2          | sd_card_cdata0_2_pad_in       | 1             | no                          | sd_card_cdata0_2_pad_out          | sd_card_cdata0_2_pad_oe                      | no                           |
| 3          | sd_card_cdata1_2_pad_in       | 1             | no                          | sd_card_cdata1_2_pad_out          | sd_card_cdata1_2_pad_oe                      | no                           |
| 4          | sd_card_cdata2_2_pad_in       | 1             | no                          | sd_card_cdata2_2_pad_out          | sd_card_cdata2_2_pad_oe                      | no                           |
| 5          | sd_card_cdata3_2_pad_in       | 1             | no                          | sd_card_cdata3_2_pad_out          | sd_card_cdata3_2_pad_oe                      | no                           |
| 6          | sd_card_cdata4_2_pad_in       | 1             | no                          | sd_card_cdata4_2_pad_out          | sd_card_cdata4_2_pad_oe                      | no                           |
| 7          | sd_card_cdata5_2_pad_in       | 1             | no                          | sd_card_cdata5_2_pad_out          | sd_card_cdata5_2_pad_oe                      | no                           |
| 8          | sd_card_cdata6_2_pad_in       | 1             | no                          | sd_card_cdata6_2_pad_out          | sd_card_cdata6_2_pad_oe                      | no                           |
| 9          | sd_card_cdata7_2_pad_in       | 1             | no                          | sd_card_cdata7_2_pad_out          | sd_card_cdata7_2_pad_oe                      | no                           |
| 10         | uart0_rxd_pad_in              | 0             | yes                         | uart0_txd_pad_out                 | 'd1                                          | yes                          |
| 11         | uart0_cts_pad_in              | 0             | yes                         | uart0_rts_pad_out                 | 'd1                                          | yes                          |
| 12         | uart0_dsr_pad_in              | 0             | no                          | uart0_dtr_pad_out                 | 'd1                                          | no                           |
| 13         | uart1_rxd_pad_in              | 0             | yes                         | uart1_txd_pad_out                 | 'd1                                          | yes                          |
| 14         | uart1_cts_pad_in              | 0             | yes                         | uart1_rts_pad_out                 | 'd1                                          | yes                          |
| 15         | uart1_dsr_pad_in              | 0             | no                          | uart1_dtr_pad_out                 | 'd1                                          | no                           |
| 16         | uart2_rxd_pad_in              | 0             | no                          | uart2_txd_pad_out                 | 'd1                                          | no                           |
| 17         | uart2_cts_pad_in              | 0             | no                          | uart2_rts_pad_out                 | 'd1                                          | no                           |
| 18         | uart2_dsr_pad_in              | 0             | no                          | uart2_dtr_pad_out                 | 'd1                                          | no                           |
| 19         | uart3_rxd_pad_in              | 0             | no                          | uart3_txd_pad_out                 | 'd1                                          | no                           |
| 20         | uart3_cts_pad_in              | 0             | no                          | uart3_rts_pad_out                 | 'd1                                          | no                           |
| 21         | uart3_dsr_pad_in              | 0             | no                          | uart3_dtr_pad_out                 | 'd1                                          | no                           |
| 22         | uart4_rxd_pad_in              | 0             | no                          | uart4_txd_pad_out                 | 'd1                                          | no                           |
| 23         | uart4_cts_pad_in              | 0             | no                          | uart4_rts_pad_out                 | 'd1                                          | no                           |
| 24         | uart4_dsr_pad_in              | 0             | no                          | uart4_dtr_pad_out                 | 'd1                                          | no                           |
| 25         | i2s0_o_bck_pad_in             | 0             | no                          | i2s0_o_bck_pad_out                | 'd1                                          | no                           |
| 26         | i2s0_mclk_pad_in              | 0             | no                          | i2s0_mclk_pad_out                 | 'd1                                          | no                           |
```