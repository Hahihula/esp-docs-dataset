

```markdown
| Signal No. | Input Signal       | Default Value | Direct Input via HP IO MUX | Output Signal   | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|--------------------|---------------|-----------------------------|-----------------|--------------------------------------------------|------------------------------|
| 83         | pwmO_f0_in         | 0             | no                          | pwmO_out1b      | 'd1                                              | no                           |
| 84         | pwmO_f1_in         | 0             | no                          | pwmO_out2a      | 'd1                                              | no                           |
| 85         | pwmO_f2_in         | 0             | no                          | pwmO_out2b      | 'd1                                              | no                           |
| 86         | pwmO_capO_in       | 0             | no                          | par_tx_cs_o     | 'd1                                              | no                           |
| 87         | pwmO_cap1_in       | 0             | no                          | —               | —                                                | —                            |
| 88         | pwmO_cap2_in       | 0             | no                          | —               | —                                                | —                            |
| 89         | —                  | —             | —                           | —               | —                                                | —                            |
| 90         | —                  | —             | —                           | —               | —                                                | —                            |
| 91         | —                  | —             | —                           | —               | —                                                | —                            |
| 92         | —                  | —             | —                           | —               | —                                                | —                            |
| 93         | —                  | —             | —                           | —               | —                                                | —                            |
| 94         | —                  | —             | —                           | —               | —                                                | —                            |
| 95         | —                  | —             | —                           | —               | —                                                | —                            |
| 96         | —                  | —             | —                           | —               | —                                                | —                            |
| 97         | sig_in_func_97     | 0             | no                          | sig_in_func97   | 'd1                                              | no                           |
| 98         | sig_in_func_98     | 0             | no                          | sig_in_func98   | 'd1                                              | no                           |
| 99         | sig_in_func_99     | 0             | no                          | sig_in_func99   | 'd1                                              | no                           |
| 100        | sig_in_func_100    | 0             | no                          | sig_in_func100  | 'd1                                              | no                           |
| 101        | pcnt_sig_chO_inO   | 0             | no                          | FSPICS1_out     | FSPICS1_oE                                      | yes                          |
| 102        | pcnt_sig_ch1_inO   | 0             | no                          | FSPICS2_out     | FSPICS2_oE                                      | yes                          |
| 103        | pcnt_ctrl_chO_inO  | 0             | no                          | FSPICS3_out     | FSPICS3_oE                                      | yes                          |
| 104        | pcnt_ctrl_ch1_inO  | 0             | no                          | FSPICS4_out     | FSPICS4_oE                                      | yes                          |
| 105        | pcnt_sig_chO_in1   | 0             | no                          | FSPICS5_out     | FSPICS5_oE                                      | yes                          |
| 106        | pcnt_sig_ch1_in1   | 0             | no                          | —               | —                                                | —                            |
| 107        | pcnt_ctrl_chO_in1  | 0             | no                          | —               | —                                                | —                            |
| 108        | pcnt_ctrl_ch1_in1  | 0             | no                          | —               | —                                                | —                            |
| 109        | pcnt_sig_chO_in2   | 0             | no                          | —               | —                                                | —                            |
| 110        | pcnt_sig_ch1_in2   | 0             | no                          | —               | —                                                | —                            |
```