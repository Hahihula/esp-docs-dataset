

```markdown
- Manual-invalidate operation only works on the unlocked data. If you plan to perform this operation on the locked data, please unlock them first.
```

## 6.3.4 GDMA Address Space

The General Direct Memory Access (GDMA) peripheral in ESP32-C5 consisting of three TX channels and three RX channels provides Direct Memory Access (DMA) service, including:

- data transfers between different locations of internal memory
- data transfers between modules/peripherals and internal memory
- data transfers between different locations of external memory
- data transfers between modules/peripherals and external memory
- data transfers between internal memory and external memory

GDMA uses the same addresses as the data bus to access HP SRAM and external RAM, i.e., GDMA uses address range 0x4080_0000 ~ 0x4085_FFFF to access HP SRAM, and 0x4200_0000 ~ 0x43FF_FFFF to external RAM. Seven modules/peripherals in ESP32-C5 work together with GDMA. As shown in Figure 6.3-4, seven vertical lines correspond to these seven modules/peripherals with GDMA function. The horizontal line represents a certain channel of GDMA (can be any channel), and the intersection of the vertical line and the horizontal line indicates that a module/peripheral has the ability to access the corresponding channel of GDMA.

![Figure 6.3-4. Modules/peripherals that can work with GDMA](image)

```markdown
These modules/peripherals can access any memory available to GDMA. For more information, please refer to Chapter 5 GDMA Controller (GDMA).
```
```