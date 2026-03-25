

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_PIN27_REG                             | GPIO27 pin configuration register                                          | 0x00E0    | R/W    |

**Input Configuration Registers**

|                                    | Configuration register for input signal 0 | 0x0154   | R/W    |
|--------------------------------------|--------------------------------------------|----------|--------|
| GPIO_FUNCN_IN_SEL_CFG_REG            |                                            | 0x0158   | R/W    |
| GPIO_FUNC2_IN_SEL_CFG_REG             |                                            | 0x015C   | R/W    |
| ...                                  | ...                                        | ...      | ...    |
| GPIO_FUNC125_IN_SEL_CFG_REG           |                                            | 0x0348   | R/W    |
| GPIO_FUNC126_IN_SEL_CFG_REG            |                                            | 0x034C   | R/W    |
| GPIO_FUNC127_IN_SEL_CFG_REG             |                                            | 0x0350   | R/W    |

**Output Configuration Registers**

|                                    | Configuration register for GPIO0 output | 0x0554   | varies |
|--------------------------------------|-------------------------------------------|----------|--------|
| GPIO_FUNCO_OUT_SEL_CFG_REG           |                                           | 0x0558   | varies |
| GPIO_FUNC1_OUT_SEL_CFG_REG            |                                           | 0x055C   | varies |
| GPIO_FUNC2_OUT_SEL_CFG_REG             |                                           | 0x055C   | varies |
| ...                                  | ...                                       | ...      | ...    |
| GPIO_FUNC25_OUT_SEL_CFG_REG           |                                           | 0x05B8   | varies |
| GPIO_FUNC26_OUT_SEL_CFG_REG            |                                           | 0x05BC   | varies |
| GPIO_FUNC27_OUT_SEL_CFG_REG             |                                           | 0x05C0   | varies |

**Version Register**

|                                    | GPIO version register                     | 0x06FC   | R/W    |

**Clock Gate Register**

|                                    | GPIO clock gate register                  | 0x062C   | R/W    |
```

## 6.17.2 IO MUX Register Summary

The addresses in this section are relative to the IO MUX base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

For ESP32-H2, 19 GPIO pins are available, i.e., GPIO0 ~ GPIO5, GPIO8 ~ GPIO14 and GPIO22 ~ GPIO27. For this case, Configuration Registers of IO_MUX_GPIO6_REG ~ IO_MUX_GPIO7_REG and IO_MUX_GPIO15_REG ~ IO_MUX_GPIO21_REG are not configurable.

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                             |           |        |
| IO_MUX_PIN_CTRL_REG                        | Clock output configuration register                                        | 0x0000    | R/W    |
| IO_MUX_GPIO0_REG                           | IO MUX configuration register for GPIO0                                    | 0x0004    | R/W    |
| IO_MUX_GPIO1_REG                            | IO MUX configuration register for GPIO1                                    | 0x0008    | R/W    |
| IO_MUX_GPIO2_REG                             | IO MUX configuration register for GPIO2                                    | 0x000C    | R/W    |
| ...                                        | ...                                                                         | ...       | ...    |
| IO_MUX_GPIO25_REG                           | IO MUX configuration register for GPIO25                                   | 0x0068    | R/W    |
| IO_MUX_GPIO26_REG                            | IO MUX configuration register for GPIO26                                   | 0x006C    | R/W    |
| IO_MUX_GPIO27_REG                             | IO MUX configuration register for GPIO27                                   | 0x0070    | R/W    |

**Version Register**

|                                    | Version control register                                                        |           |        |
|--------------------------------------|-------------------------------------------------------------------------------|-----------|--------|
| IO_MUX_DATE_REG                      |                                                                                   | 0x00FC    | R/W    |
```