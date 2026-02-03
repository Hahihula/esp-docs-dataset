**Appendix A**

---

**A.2. GPIO_Matrix**

*In Table GPIO_Matrix, the column “Default Value if unassigned” records the default value of an input signal if no GPIO is assigned to it. The actual value is determined by register GPIO_FUNCm_IN_INV_SEL and GPIO_FUNCm_IN_SEL. (The value of m ranges from 1 to 255.)*

---

**Table 6-2. GPIO_Matrix**

| Signal | No. Input Signals | Default Value If Unassigned* | Same Input Signal from IO_MUX Core | Output Signals |
|--------|------------------|------------------------------|-------------------------------------|---------------|
| O      | SPICLK_in        | 0                            | yes                                  | SPICLK_out   |
|       |                  |                              |                                     | SPICLK_oe    |
| 1      | SPIQ_in          | 0                            | yes                                  | SPIQ_out     |
|       |                  |                              |                                     | SPIQE_out    |
| 2      | SPID_in          | 0                            | yes                                  | SPID_out     |
|       |                  |                              |                                     | SPIOD_out    |
| 3      | SPIHD_in         | 0                            | yes                                  | SPIHD_out    |
|       |                  |                              |                                     | SPIHDE_out   |
| 4      | SPIWP_in         | 0                            | yes                                  | SPIWP_out    |
|       |                  |                              |                                     | SPIWPE_out   |
| 5      | SPICS0_in        | 0                            | yes                                  | SPICS0_out   |
|       |                  |                              |                                     | SPICSO_out   |
| 6      | SPICS1_in        | O                            | no                                   | SPICS1_out   |
|       |                  |                              |                                     | SPICS1E_out  |
| 7      | SPICS2_in        | O                            | no                                   | SPICS2_out   |
|       |                  |                              |                                     | SPICS2E_out  |
| 8      | HSPICLK_in       | O                            | yes                                  | HSPICLK_out  |
|       |                  |                              |                                     | HSPICLKOE_out|
| 9      | HSPIQ_in         | O                            | yes                                  | HSPIQ_out    |
|       |                  |                              |                                     | HSPIQE_out   |
| 10     | HSPID_in         | O                            | yes                                  | HSPID_out    |
|       |                  |                              |                                     | HSPIOD_out   |
| 11     | HSPICS0_in       | O                            | yes                                  | HSPICS0_out  |
|       |                  |                              |                                     | HSPICSOE_out |
| 12     | HSPIHD_in        | O                            | yes                                  | HSPIHD_out   |
|       |                  |                              |                                     | HSPIHDE_out  |
| 13     | HSPIWP_in        | O                            | yes                                  | HSPIWP_out   |
|       |                  |                              |                                     | HSPICWOE_out |
| 14     | UORXD_in         | O                            | yes                                  | UOTXD_out    |
|       |                  |                              |                                     | UOTXDOE_out  |
| 15     | UOCTS_in         | O                            | yes                                  | UORTS_out    |
|       |                  |                              |                                     | UORTSOE_out  |
| 16     | UODSR_in         | O                            | no                                   | UODTR_out    |
|       |                  |                              |                                     | UOTROE_out   |
| 17     | UIRXD_in         | O                            | yes                                  | UITXD_out    |
|       |                  |                              |                                     | UITXDOE_out  |
| 18     | UICTS_in         | O                            | yes                                  | UIRTS_out    |
|       |                  |                              |                                     | UIORTSOE_out|
| 23     | I2S0O_BCK_in     | O                            | no                                   | I2S0OBCK_out |
|       |                  |                              |                                     | I2S0BCKOE_out|
| 24     | I2S1O_BCK_in     | O                            | yes                                  | I2S1OBCK_out |
|       |                  |                              |                                     | I2S1BCKOE_out|
| 25     | I2S0O_WS_in      | O                            | no                                   | I2S0OWS_out  |
|       |                  |                              |                                     | I2S0WS_out   |
| 26     | I2S1O_WS_in      | O                            | yes                                  | I2S1OWS_out  |
|       |                  |                              |                                     | I2S1WS_out   |
| 27     | I2SOI_BCK_in     | O                            | no                                   | I2SOIBCK_out |
|       |                  |                              |                                     | I2SOIBCKOE_out|
| 28     | I2SOI_WS_in      | O                            | yes                                  | I2SOWS_out   |
|       |                  |                              |                                     | I2SOWS_out   |
| 29     | I2CEXTO_SCL_in   | 1                            | no                                   | I2CEXTOSCL_out|
|       |                  |                              |                                     | I2CEXTSOE_out|
| 30     | I2CEXTO_SDA_in   | O                            | yes                                  | I2CEXTOSDA_out|
|       |                  |                              |                                     | I2CEXTSADOE_out|
| 31     | pwm0_sync0_in    | O                            | no                                   | pvm0_out0a   |
|       |                  |                              |                                     | pvm0out0aOE_out|
| 32     | pwm0_sync1_in    | O                            | yes                                  | pvm0_out0b   |
|       |                  |                              |                                     | pvm0out0BOE_out|

---

**Espressif Systems**

**Submit Documentation Feedback**

**ESP32 Series Datasheet v5.2, Page 64**