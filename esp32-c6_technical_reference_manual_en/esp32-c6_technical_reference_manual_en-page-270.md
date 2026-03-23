

```markdown\n| Name | Description | Address | Access |\n| :------------------------ | :--------------------------------------------- | :------- | :------ |\n| LP_IO_PIN1_REG | LP GPIO1 configuration register | 0x002C | R/W |\n| LP_IO_PIN2_REG | LP GPIO2 configuration register | 0x0030 | R/W |\n| LP_IO_PIN3_REG | LP GPIO3 configuration register | 0x0034 | R/W |\n| LP_IO_PIN4_REG | LP GPIO4 configuration register | 0x0038 | R/W |\n| LP_IO_PIN5_REG | LP GPIO5 configuration register | 0x003C | R/W |\n| LP_IO_PIN6_REG | LP GPIO6 configuration register | 0x0040 | R/W |\n| LP_IO_PIN7_REG | LP GPIO7 configuration register | 0x0044 | R/W |\n| **GPIO LP Function Configuration Registers** |  |  |  |\n| LP_IO_GPIO0_REG | LP IO MUX configuration register for GPIO0 | 0x0048 | R/W |\n| LP_IO_GPIO1_REG | LP IO MUX configuration register for GPIO1 | 0x004C | R/W |\n| LP_IO_GPIO2_REG | LP IO MUX configuration register for GPIO2 | 0x0050 | R/W |\n| LP_IO_GPIO3_REG | LP IO MUX configuration register for GPIO3 | 0x0054 | R/W |\n| LP_IO_GPIO4_REG | LP IO MUX configuration register for GPIO4 | 0x0058 | R/W |\n| LP_IO_GPIO5_REG | LP IO MUX configuration register for GPIO5 | 0x005C | R/W |\n| LP_IO_GPIO6_REG | LP IO MUX configuration register for GPIO6 | 0x0060 | R/W |\n| LP_IO_GPIO7_REG | LP IO MUX configuration register for GPIO7 | 0x0064 | R/W |\n| LP_IO_STATUS_INT_REG | LP GPIO interrupt source register | 0x0068 | RO |\n| **Version Register** |  |  |  |\n| LP_IO_DATE_REG | Version control regiter | 0x03FC | R/W |\n\n## 7.16 Registers\n### 7.16.1 GPIO Matrix Registers\nThe addresses in this section are relative to GPIO base address provided in Table 5.3-2 in Chapter 5 System and Memory.\n\n**Register 7.1. GPIO_OUT_REG (0x0004)**\n```
```markdown
31                                 0
+-----------------------------+
|        0x000000             | Reset
+-----------------------------+

GPIO_OUT_DATA_ORIG Configures the output value of GPIO0 ~ 30 output in simple GPIO output mode.
O: Low level
1: High level
The value of bit0 ~ bit30 correspond to the output value of GPIO0 ~ GPIO30 respectively. Bit31 is invalid.
(R/W/SC/WTC)
```