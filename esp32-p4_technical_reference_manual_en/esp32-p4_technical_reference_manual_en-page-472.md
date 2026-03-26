

```markdown
- Supports up to 64 MB of external flash and RAM
• Peripheral Space
    – 96 modules/peripherals in total
• GDMA
    – 7 GDMA-AHB supported modules/peripherals
    – 6 GDMA-AXI supported modules/peripherals

## 7.3 Functional Description

### 7.3.1 Address Mapping

Figure 7.3-1 illustrates the system structure and address mapping. All the non-reserved addresses are accessible via both the instruction bus and the data bus, meaning that the instruction bus and the data bus share the same address space.

Both the data bus and instruction bus of the HP CPU and LP CPU are little-endian. However, the HP CPU’s data bus (DBUS) has a 128-bit data width, while other buses maintain a 32-bit data width.

The HP CPU can access data via the data bus using single-byte, double-byte, 4-byte alignment, and, in case of AI Instruction, up to 16-byte alignment. The LP CPU can access data via the data bus using single-byte, double-byte, and 4-byte alignment.

The HP CPU has the following access capabilities:

• Direct access to HP SPM via both the data bus and instruction bus.
• Access to internal memory and external memory mapped into the address space via cache, including:
    – 128 KB HP ROM (0x4FC0_0000 ~ 0x4FC1_FFFF)
    – 768 KB HP L2MEM (0x4FF0_0000 ~ 0x4FFB_FFFF)
    – 64 MB external flash (0x4000_0000 ~ 0x43FF_FFFF)
    – 64 MB external RAM (0x4800_0000 ~ 0x4BFF_FFFF)

**Note:**
Software can use the addresses starting with “0x4” in two ways: cache-able access or noncache-able access, depending on the control of CPU Physical Memory Attribution (PMA). Cache-able access is done via cache. Noncache-able access is done without cache, which is similar to the direct access to the addresses starting with “0x8”, however, such direct access to “0x8” addresses is usually for debugging.

• Direct access to internal memory and external memory mapped into the following address space without cache. This access is slower than that via cache.
    – 128 KB HP ROM (0x8FC0_0000 ~ 0x8FC1_FFFF)
    – 768 KB HP L2MEM (0x8FF0_0000 ~ 0x8FFB_FFFF)
    – 32 KB LP SRAM (0x5010_8000 ~ 0x5010_FFFF)
```