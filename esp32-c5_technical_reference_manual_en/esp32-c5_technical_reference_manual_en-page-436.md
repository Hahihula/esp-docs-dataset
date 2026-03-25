

```markdown
Register 9.53. PCR_ECC_PD_CTRL_REG (0x00E0)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                    |                                                                             |
| 3   | PCR_ECC_MEM_FORCE_PD       | Configures whether or not to force power down ECC internal memory.          |
|     |                             | 0: Not force power down                                                     |
|     |                             | 1: Force power down                                                          |
|     | (R/W)                       |                                                                             |
| 2   | PCR_ECC_MEM_FORCE_PU       | Configures whether or not to force power up ECC internal memory.            |
|     |                             | 0: Not force power up                                                        |
|     |                             | 1: Force power up                                                            |
|     | (R/W)                       |                                                                             |
| 1   | PCR_ECC_MEM_PD             | Configures whether or not to power down ECC internal memory.                |
|     |                             | 0: Not power down                                                           |
|     |                             | 1: Power down                                                               |
|     | (R/W)                       |                                                                             |
```