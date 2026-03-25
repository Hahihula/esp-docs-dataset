

```markdown
|Name|Description|Address|Access|
|:-----------------------------|:------------------------------------------------------------------------------------------------------------------------|:--------|:---------|
|Configuration Registers||||
|GPIO_OUT_REG|GPIO output register|0x0004|R/W/SC/WTC|
|GPIO_OUT_W1TS_REG|GPIO output set register|0x0008|WT|
|GPIO_OUT_W1TC_REG|GPIO output clear register|0x000C|WT|
|GPIO_ENABLE_REG|GPIO output enable register|0x0020|R/W/WT/C|
|GPIO_ENABLE_W1TS_REG|GPIO output enable set register|0x0024|WT|
|GPIO_ENABLE_W1TC_REG|GPIO output enable clear register|0x0028|WT|
|GPIO_STRAP_REG|Strapping pin register|0x0038|RO|
|GPIO_IN_REG|GPIO input register|0x003C|RO|
|Interrupt Status Registers||||
|GPIO_STATUS_REG|GPIO interrupt status register|0x0044|R/W/WT/C|
|GPIO_STATUS_W1TS_REG|GPIO interrupt status set register|0x0048|WT|
|GPIO_STATUS_W1TC_REG|GPIO interrupt status clear register|0x004C|WT|
|GPIO_PCPU_INT_REG|GPIO CPU interrupt status register|0x005C|RO|
|GPIO_STATUS_NEXT_REG|GPIO interrupt source register|0x014C|RO|
|Pin Configuration Registers||||
|GPIO_PIN0_REG|GPIO0 configuration register|0x0074|R/W|
|GPIO_PIN1_REG|GPIO1 configuration register|0x0078|R/W|
|GPIO_PIN2_REG|GPIO2 configuration register|0x007C|R/W|
|...|...|...|...|
|GPIO_PIN25_REG|GPIO25 pin configuration register|0x00D8|R/W|
|GPIO_PIN26_REG|GPIO26 pin configuration register|0x00DC|R/W|
```