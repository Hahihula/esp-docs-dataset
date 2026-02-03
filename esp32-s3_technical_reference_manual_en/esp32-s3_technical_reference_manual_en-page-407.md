**Chapter Title:**
Chapter 4 System and Memory

**Body Text:**

In addition, GDMA can access the external memory (only RAM) via the same address as CPU accessing DCache (0x3C00_0000 ~ 0x3DFF_FFFF). When DCache and GDMA access the external memory simultaneously, the software needs to make sure the data is consistent.

Besides, some peripherals/modules of the ESP32-S3 can work together with GDMA. In these cases, GDMA can provide the following powerful services for them:

- Data transfers between modules/peripherals and internal memory;
- Data transfers between modules/peripherals and external memory.

There are 10 peripherals/modules that can work together with GDMA. As shown in Figure 4.3-2, these 10 vertical lines in turn correspond to these 10 peripherals/modules with GDMA function; the horizontal line represents a certain channel of GDMA (can be any channel), and the intersection of the vertical line and the horizontal line indicates that a peripheral/module has the ability to access the corresponding channel of GDMA. If there are multiple intersections on the same line, it means that these peripherals/modules cannot enable the GDMA function at the same time.

**Figure Description:**
- Figure 4.3-2 Peripherals/modules that can work with b GDMA

**Figure Caption and Notes:**
*Note: UART0, UART1, and UART2 support DMA functionality via UHCIO.*

These peripherals/modules can access any memory available to GDMA. For more information, please refer to Chapter 3 GDMA Controller (GDMA).

**Additional Note in Boxed Text:**
- When accessing a memory via GDMA, a corresponding access permission is needed; otherwise this access may fail.
- For more information about permission control, please refer to Chapter 15 Permission Control (PMS).

**Subsection Title and Content:**

4.3.5 Modules/Peripherals

The CPU can access modules/peripherals via 0x6000_0000 ~ 0x600D_OFFF shared by the data/instruction bus.

**Footer Information:**
- Espressif Systems
- Document Version and Submission Link:
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback