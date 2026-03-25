

```markdown
Register 7.14. PCR_LEDC_PD_CTRL_REG (0x003C)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 3   | PCR_LEDC_MEM_FORCE_PD                                                     |
| 2   | PCR_LEDC_MEM_FORCE_PU                                                      |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                       |

PCR_LEDC_MEM_FORCE_PU Configures whether or not to force power up LEDC memory.
- 0: Not force power up LEDC memory
- 1: Force power up LEDC memory
(R/W)

PCR_LEDC_MEM_FORCE_PD Configures whether or not to force power down LEDC memory.
- 0: Not force power down LEDC memory
- 1: Force power down LEDC memory
(R/W)
```