

```markdown
Chapter 4 System and Memory

GoBack

4.3.1 Address Mapping

Figure 4.3-1 illustrates the system structure and address mapping. All the non-reserved addresses are accessible via both the instruction bus and the data bus, meaning that the instruction bus and the data bus share the same address space.

Both the data bus and instruction bus of the CPU are little-endian. All buses have a 32-bit data width. The CPU can access data via the data bus using single-byte, double-byte, and 4-byte alignment.

The CPU has the following access capabilities:

* Direct access to internal memory via both the data bus and instruction bus
    - 320 KB HP SRAM (0x4080_0000~0x4084_FFFF)
    - 256 KB ROM (0x4000_0000~0x4003_FFFF)

* Access to external memory through the cache
    The virtual address is mapped to the physical address space of the external memory through the MMU.
        - Up to 32 MB external flash (0x4200_0000~0x43FF_FFFF)
        - Up to 32 MB external RAM (0x4200_0000~0x43FF_FFFF)

* Direct access to modules/peripherals via the data bus, including:
    - CPU Peripherals
    - HP Peripherals
    - LP Peripherals
```