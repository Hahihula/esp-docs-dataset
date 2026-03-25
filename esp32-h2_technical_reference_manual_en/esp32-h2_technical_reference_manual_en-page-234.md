

```markdown
| Signal No.| Input Signal          | Default value | Direct Input via IO MUX | Output Signal   | Output enable signal when GPIO_FUNCn_OEN_SEL = 0 | Direct Output via IO MUX |
|-----------|-----------------------|---------------|-------------------------|-----------------|--------------------------------------------------|--------------------------|
| 110       | pcnt_sig_ch1_in2      | 0             | no                      | cte_ant14       | 1'd1                                              | no                       |
| 111       | pcnt_ctrl_chO_in2     | 0             | no                      | cte_ant15       | 1'd1                                              | no                       |
| 112       | pcnt_ctrl_ch1_in2     | 0             | no                      | -               | -                                                | -                        |
| 113       | pcnt_sig_chO_in3      | 0             | no                      | -               | -                                                | -                        |
| 114       | pcnt_sig_ch1_in3      | 0             | no                      | SPICLK_out_mux  | SPICLK_oe                                        | yes                      |
| 115       | pcnt_ctrl_chO_in3     | 0             | no                      | SPICS0_out      | SPICS0_oe                                        | yes                      |
| 116       | pcnt_ctrl_ch1_in3     | 0             | no                      | SPICS1_out      | SPICS1_oe                                        | no                       |
| 117       | -                     | -             | -                       | -               | -                                                | -                        |
| 118       | -                     | -             | -                       | -               | -                                                | -                        |
| 119       | -                     | -             | -                       | -               | -                                                | -                        |
| 120       | -                     | -             | -                       | -               | -                                                | -                        |
| 121       | SPIQ_in               | 0             | yes                     | SPIQ_out        | SPIQ_oe                                          | yes                      |
| 122       | SPID_in               | 0             | yes                     | SPID_out        | SPID_oe                                          | yes                      |
| 123       | SPIHD_in              | 0             | yes                     | SPIHD_out       | SPIHD_oe                                         | yes                      |
| 124       | SPIWP_in              | 0             | yes                     | SPIWP_out       | SPIWP_oe                                         | yes                      |
| 125       | -                     | -             | -                       | CLK_OUT_out1    | 1'd1                                              | no                       |
| 126       | -                     | -             | -                       | CLK_OUT_out2    | 1'd1                                              | no                       |
| 127       | -                     | -             | -                       | CLK_OUT_out3    | 1'd1                                              | no                       |
```