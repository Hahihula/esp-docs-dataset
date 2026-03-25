

```markdown
Chapter 22 RSA Accelerator (RSA)

Register 22.4. RSA_SET_START_MODMULT_REG (0x0810)


31 | [reserved] | RSA_SET_START_MODMULT_REG |
|----:|:-----------|--------------------------|
|    |            | Reset                    |
|    |            | 0                        |

RSA_SET_START_MODMULT Configures whether or not to start the modular multiplication.
O: No effect
1: Start
(WT)

Register 22.5. RSA_SET_START_MULT_REG (0x0814)


31 | [reserved] | RSA_SET_START_MULT_REG |
|----:|:-----------|------------------------|
|    |            | Reset                  |
|    |            | 0                      |

RSA_SET_START_MULT Configures whether or not to start the multiplication.
O: No effect
1: Start
(WT)

Register 22.6. RSA_QUERY_IDLE_REG (0x0818)


31 | [reserved] | RSA_QUERY_IDLE_REG |
|----:|:-----------|---------------------|
|    |            | Reset               |
|    |            | 0                   |

RSA_QUERY_IDLE Represents the RSA status.
O: Busy
1: Idle
(RO)
```