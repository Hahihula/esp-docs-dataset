

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_FUNC11_OUT_SEL_CFG_REG               | Configuration register for GPIO11 output                                    | 0x0AFO    | varies |
| GPIO_FUNC12_OUT_SEL_CFG_REG               | Configuration register for GPIO12 output                                    | 0x0AF4    | varies |
| GPIO_FUNC13_OUT_SEL_CFG_REG               | Configuration register for GPIO13 output                                    | 0x0AF8    | varies |
| GPIO_FUNC14_OUT_SEL_CFG_REG               | Configuration register for GPIO14 output                                    | 0x0AFC    | varies |
| GPIO_FUNC23_OUT_SEL_CFG_REG               | Configuration register for GPIO23 output                                    | 0x0B20    | varies |
| GPIO_FUNC24_OUT_SEL_CFG_REG               | Configuration register for GPIO24 output                                    | 0x0B24    | varies |
| GPIO_FUNC25_OUT_SEL_CFG_REG               | Configuration register for GPIO25 output                                    | 0x0B28    | varies |
| GPIO_FUNC26_OUT_SEL_CFG_REG               | Configuration register for GPIO26 output                                    | 0x0B2C    | varies |
| GPIO_FUNC27_OUT_SEL_CFG_REG               | Configuration register for GPIO27 output                                    | 0x0B30    | varies |
| GPIO_FUNC28_OUT_SEL_CFG_REG               | Configuration register for GPIO28 output                                    | 0x0B34    | varies |

Clock Gate Register
| Name                  | Description       | Address   | Access |
|-----------------------|-------------------|-----------|--------|
| GPIO_CLOCK_GATE_REG  | GPIO clock gate register | 0x0DF8   | R/W    |

Version Register
| Name              | Description     | Address   | Access |
|-------------------|-----------------|-----------|--------|
| GPIO_DATE_REG     | GPIO version register | 0x0DFC   | R/W    |
```

## 8.18.2 HP IO MUX Register Summary

The addresses in this section are relative to the HP IO MUX base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

```markdown
| Name                  | Description                                                                 | Address   | Access |
|-----------------------|-----------------------------------------------------------------------------|-----------|--------|
| Configuration Registers |                                                                             |           |        |
| IO_MUX_GPIO0_REG     | IO MUX configuration register for GPIO0                                    | 0x0000    | R/W    |
| IO_MUX_GPIO1_REG     | IO MUX configuration register for GPIO1                                    | 0x0004    | R/W    |
| IO_MUX_GPIO2_REG     | IO MUX configuration register for GPIO2                                    | 0x0008    | R/W    |
| IO_MUX_GPIO3_REG     | IO MUX configuration register for GPIO3                                    | 0x000C    | R/W    |
| IO_MUX_GPIO4_REG     | IO MUX configuration register for GPIO4                                    | 0x0010    | R/W    |
| IO_MUX_GPIO5_REG     | IO MUX configuration register for GPIO5                                    | 0x0014    | R/W    |
| IO_MUX_GPIO6_REG     | IO MUX configuration register for GPIO6                                    | 0x0018    | R/W    |
| IO_MUX_GPIO7_REG     | IO MUX configuration register for GPIO7                                    | 0x001C    | R/W    |
| IO_MUX_GPIO8_REG     | IO MUX configuration register for GPIO8                                    | 0x0020    | R/W    |
| IO_MUX_GPIO9_REG     | IO MUX configuration register for GPIO9                                    | 0x0024    | R/W    |
| IO_MUX_GPIO10_REG    | IO MUX configuration register for GPIO10                                   | 0x0028    | R/W    |
| IO_MUX_GPIO11_REG    | IO MUX configuration register for GPIO11                                   | 0x002C    | R/W    |
| IO_MUX_GPIO12_REG    | IO MUX configuration register for GPIO12                                   | 0x0030    | R/W    |
| IO_MUX_GPIO13_REG    | IO MUX configuration register for GPIO13                                   | 0x0034    | R/W    |
| IO_MUX_GPIO14_REG    | IO MUX configuration register for GPIO14                                   | 0x0038    | R/W    |
| IO_MUX_GPIO23_REG    | IO MUX configuration register for GPIO23                                   | 0x005C    | R/W    |
| IO_MUX_GPIO24_REG    | IO MUX configuration register for GPIO24                                   | 0x0060    | R/W    |
| IO_MUX_GPIO25_REG    | IO MUX configuration register for GPIO25                                   | 0x0064    | R/W    |
| IO_MUX_GPIO26_REG    | IO MUX configuration register for GPIO26                                   | 0x0068    | R/W    |
| IO_MUX_GPIO27_REG    | IO MUX configuration register for GPIO27                                   | 0x006C    | R/W    |
```