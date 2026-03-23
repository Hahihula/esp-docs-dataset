

```markdown
Please note that Manual-Invalidate operation only works on the unlocked data. If you expect to perform such operation on the locked data, please unlock them first.

## 5.3.4 GDMA Address Space

The General Direct Memory Access (GDMA) peripheral consisting of three TX channels and three RX channels provides Direct Memory Access (DMA) service, including:

*   data transfers between different locations of internal memory
*   data transfers between modules/peripherals and internal memory

GDMA uses the same addresses as the data bus to access HP SRAM, i.e., GDMA uses address range `0x4080_0000 ~ 0x4087_FFFF` to access HP SRAM.

Eight modules/peripherals in ESP32-C6 work together with GDMA. As shown in Figure 5.3-2, eight vertical lines correspond to these eight modules/peripherals with GDMA function. The horizontal line represents a certain channel of GDMA (can be any channel), and the intersection of the vertical line and the horizontal line indicates that a module/peripheral has the ability to access the corresponding channel of GDMA. If there are multiple intersections on the same line, it means that these peripherals/modules can not enable the GDMA function at the same time.

![Figure 5.3-2. Modules/peripherals that can work with GDMA](image)

These modules/peripherals can access any memory available to GDMA. For more information, please refer to Chapter 4 GDMA Controller (GDMA).

**Note:**
When accessing a memory via GDMA, a corresponding access permission is needed, otherwise this access may fail.
For more information about permission control, please refer to Chapter 16 Permission Control (PMS).
```