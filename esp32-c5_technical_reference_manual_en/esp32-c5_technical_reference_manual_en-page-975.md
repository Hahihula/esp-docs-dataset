

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Plaintext Register Heap**                |                                                                             |           |        |
| XTS_AES_PLAIN_0_REG                        | Plaintext register 0                                                         | 0x0300    | R/W    |
| XTS_AES_PLAIN_1_REG                         | Plaintext register 1                                                         | 0x0304    | R/W    |
| XTS_AES_PLAIN_2_REG                         | Plaintext register 2                                                         | 0x0308    | R/W    |
| XTS_AES_PLAIN_3_REG                         | Plaintext register 3                                                         | 0x030C    | R/W    |
| XTS_AES_PLAIN_4_REG                         | Plaintext register 4                                                         | 0x0310    | R/W    |
| XTS_AES_PLAIN_5_REG                         | Plaintext register 5                                                         | 0x0314    | R/W    |
| XTS_AES_PLAIN_6_REG                         | Plaintext register 6                                                         | 0x0318    | R/W    |
| XTS_AES_PLAIN_7_REG                         | Plaintext register 7                                                         | 0x031C    | R/W    |
| XTS_AES_PLAIN_8_REG                         | Plaintext register 8                                                         | 0x0320    | R/W    |
| XTS_AES_PLAIN_9_REG                         | Plaintext register 9                                                         | 0x0324    | R/W    |
| XTS_AES_PLAIN_10_REG                        | Plaintext register 10                                                        | 0x0328    | R/W    |
| XTS_AES_PLAIN_11_REG                        | Plaintext register 11                                                        | 0x032C    | R/W    |
| XTS_AES_PLAIN_12_REG                        | Plaintext register 12                                                        | 0x0330    | R/W    |
| XTS_AES_PLAIN_13_REG                        | Plaintext register 13                                                        | 0x0334    | R/W    |
| XTS_AES_PLAIN_14_REG                        | Plaintext register 14                                                        | 0x0338    | R/W    |
| XTS_AES_PLAIN_15_REG                        | Plaintext register 15                                                        | 0x033C    | R/W    |
| **Configuration Registers**                |                                                                             |           |        |
| XTS_AES_LINESIZE_REG                        | Configures the size of target memory space                                 | 0x0340     | R/W    |
| XTS_AES_DESTINATION_REG                     | Configures the type of the external memory                                  | 0x0344     | R/W    |
| XTS_AES_PHYSICAL_ADDRESS_REG                | Stores the physical address of the external memory                         | 0x0348     | R/W    |
| XTS_AES_DPA_CTRL_REG                        | Configures the Anti-DPA function                                             | 0x0388     | R/W    |
| XTS_AES_PSEUDO_ROUND_CONF_REG               | XTS-AES pseudo-round function configuration register                       | 0x038C     | R/W    |
| **Control/status Registers**                |                                                                             |           |        |
| XTS_AES_TRIGGER_REG                         | Activates AES algorithm                                                      | 0x034C     | WT     |
| XTS_AES_RELEASE_REG                          | Releases control                                                             | 0x0350     | WT     |
| XTS_AES_DESTROY_REG                          | Destroys control                                                             | 0x0354     | WT     |
| XTS_AES_STATE_REG                            | Status register                                                              | 0x0358     | RO     |
| **Version control register**                |                                                                             |           |        |
| XTS_AES_DATE_REG                             | Version control register                                                     | 0x035C     | R/W    |
```