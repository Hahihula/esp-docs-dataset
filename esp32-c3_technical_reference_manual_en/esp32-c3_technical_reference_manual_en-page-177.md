

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_PIN15_REG                             | GPIO pin15 configuration register                                         | 0x00B0    | R/W    |
| GPIO_PIN16_REG                             | GPIO pin16 configuration register                                         | 0x00B4    | R/W    |
| GPIO_PIN17_REG                             | GPIO pin17 configuration register                                         | 0x00B8    | R/W    |
| GPIO_PIN18_REG                             | GPIO pin18 configuration register                                         | 0x00BC    | R/W    |
| GPIO_PIN19_REG                             | GPIO pin19 configuration register                                         | 0x00C0    | R/W    |
| GPIO_PIN20_REG                             | GPIO pin20 configuration register                                         | 0x00C4    | R/W    |
| GPIO_PIN21_REG                             | GPIO pin21 configuration register                                         | 0x00C8    | R/W    |

Input Function Configuration Registers
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_FUNC_IN_SEL_CFG_REG                   | Configuration register for input signal 0                                  | 0x0154    | R/W    |
| GPIO_FUNC1_IN_SEL_CFG_REG                  | Configuration register for input signal 1                                  | 0x0158    | R/W    |
| ...                                        | ...                                                                         | ...       | ...    |
| GPIO_FUNC126_IN_SEL_CFG_REG                | Configuration register for input signal 126                                | 0x034C    | R/W    |
| GPIO_FUNC127_IN_SEL_CFG_REG                | Configuration register for input signal 127                                | 0x0350    | R/W    |

Output Function Configuration Registers
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_FUNC_OUT_SEL_CFG_REG                  | Configuration register for GPIO0 output                                    | 0x0554    | R/W    |
| GPIO_FUNC1_OUT_SEL_CFG_REG                 | Configuration register for GPIO1 output                                    | 0x0558    | R/W    |
| GPIO_FUNC2_OUT_SEL_CFG_REG                 | Configuration register for GPIO2 output                                    | 0x055C    | R/W    |
| GPIO_FUNC3_OUT_SEL_CFG_REG                 | Configuration register for GPIO3 output                                    | 0x0560    | R/W    |
| GPIO_FUNC4_OUT_SEL_CFG_REG                 | Configuration register for GPIO4 output                                    | 0x0564    | R/W    |
| GPIO_FUNC5_OUT_SEL_CFG_REG                 | Configuration register for GPIO5 output                                    | 0x0568    | R/W    |
| GPIO_FUNC6_OUT_SEL_CFG_REG                 | Configuration register for GPIO6 output                                    | 0x056C    | R/W    |
| GPIO_FUNC7_OUT_SEL_CFG_REG                 | Configuration register for GPIO7 output                                    | 0x0570    | R/W    |
| GPIO_FUNC8_OUT_SEL_CFG_REG                 | Configuration register for GPIO8 output                                    | 0x0574    | R/W    |
| GPIO_FUNC9_OUT_SEL_CFG_REG                 | Configuration register for GPIO9 output                                    | 0x0578    | R/W    |
| GPIO_FUNC10_OUT_SEL_CFG_REG                | Configuration register for GPIO10 output                                   | 0x057C    | R/W    |
| GPIO_FUNC11_OUT_SEL_CFG_REG                | Configuration register for GPIO11 output                                   | 0x0580    | R/W    |
| GPIO_FUNC12_OUT_SEL_CFG_REG                | Configuration register for GPIO12 output                                   | 0x0584    | R/W    |
| GPIO_FUNC13_OUT_SEL_CFG_REG                | Configuration register for GPIO13 output                                   | 0x0588    | R/W    |
| GPIO_FUNC14_OUT_SEL_CFG_REG                | Configuration register for GPIO14 output                                   | 0x058C    | R/W    |
| GPIO_FUNC15_OUT_SEL_CFG_REG                | Configuration register for GPIO15 output                                   | 0x0590    | R/W    |
| GPIO_FUNC16_OUT_SEL_CFG_REG                | Configuration register for GPIO16 output                                   | 0x0594    | R/W    |
| GPIO_FUNC17_OUT_SEL_CFG_REG                | Configuration register for GPIO17 output                                   | 0x0598    | R/W    |
| GPIO_FUNC18_OUT_SEL_CFG_REG                | Configuration register for GPIO18 output                                   | 0x059C    | R/W    |
| GPIO_FUNC19_OUT_SEL_CFG_REG                | Configuration register for GPIO19 output                                   | 0x05A0    | R/W    |
| GPIO_FUNC20_OUT_SEL_CFG_REG                | Configuration register for GPIO20 output                                   | 0x05A4    | R/W    |
| GPIO_FUNC21_OUT_SEL_CFG_REG                | Configuration register for GPIO21 output                                   | 0x05A8    | R/W    |

Version Register
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_DATE_REG                              | GPIO version register                                                      | 0x06FC    | R/W    |

Clock Gate Register
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_CLOCK_GATE_REG                        | GPIO clock gate register                                                   | 0x062C    | R/W    |
```