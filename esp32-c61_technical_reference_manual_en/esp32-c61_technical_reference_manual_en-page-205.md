

```markdown
Chapter 4 System and Memory

GoBack

* data transfers between modules/peripherals and internal memory
* data transfers between different locations of external memory
* data transfers between modules/peripherals and external memory
* data transfers between internal memory and external memory

GDMA uses the same addresses as the data bus to access HP SRAM and external RAM, i.e., GDMA uses address range (0x4080_0000~0x4084_FFFF) to access HP SRAM, and (0x4200_0000~0x43FF_FFFF) to external RAM. Four modules/peripherals in ESP32-C61 work together with GDMA. As shown in Figure 4.3-3, four vertical lines correspond to these four modules/peripherals with GDMA function. The horizontal line represents a certain channel of GDMA (can be any channel), and the intersection of the vertical line and the horizontal line indicates that a module/peripheral has the ability to access the corresponding channel of GDMA.

![Figure 4.3-3. Modules/peripherals that can work with GDMA](image)

| SPI2 | I2S | ADC Controller | SHA Accelerator |
|------|-----|----------------|------------------|
| ●    |     |                |                  |
|      | ●   |                |                  |
|      |     | ●             |                  |
|      |     |               | ●               |

Figure 4.3-3. Modules/peripherals that can work with GDMA

These modules/peripherals can access any memory available to GDMA. For more information, please refer to Chapter 3 GDMA Controller (GDMA).

Note:
When accessing a memory via GDMA, a corresponding access permission is needed, otherwise this access may fail.
For more information about permission control, please refer to Chapter 16 Permission Control (PMS).

4.3.5 Modules/Peripherals Address Mapping

Table 4.3-2 lists all the modules/peripherals and their respective address ranges. Note that the address space of specific modules/peripherals is defined by “Boundary Address” (including both Low Address and High Address).
```