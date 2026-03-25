

```markdown
- GDMA
  - 7 GDMA-supported modules/peripherals

## 6.3 Functional Description

### 6.3.1 Address Mapping

Figure 6.3-1 illustrates the system structure and address mapping. All the non-reserved addresses are accessible via both the instruction bus and the data bus, meaning that the instruction bus and the data bus share the same address space.

Both the data bus and instruction bus of the HP CPU and LP CPU are little-endian. All buses have a 32-bit data width. HP CPU and LP CPU can access data via the data bus using single-byte, double-byte, and 4-byte alignment.

The HP CPU has the following access capabilities:

- Direct access to internal memory via both the data bus and instruction bus
  - 384 KB HP SRAM (0x4080_0000 ~ 0x4085_FFFF)
  - 16 KB LP SRAM (0x5000_0000 ~ 0x5000_3FFF)

- Access to internal memory via ROM-Cache
  - 320 KB ROM (0x4000_0000 ~ 0x4004_FFFF)

**Note:**
Software can access the ROM addresses in two ways: cache-able access or noncache-able access, depending on the control of CPU Physical Memory Attribution (PMA). Cache-able access is done via cache. Noncache-able access is done without cache.

- Access to external memory through the cache
  The virtual address is mapped to the physical address space of the external memory through the MMU.
    - Up to 32 MB external flash (0x4200_0000 ~ 0x43FF_FFFF)
    - Up to 32 MB external RAM (0x4200_0000 ~ 0x43FF_FFFF)

- Direct access to modules/peripherals via the data bus, including:
  - HP CPU Peripherals
  - HP Peripherals
  - LP Peripherals

The LP CPU has the following access capabilities:

- Direct access to HP SRAM and LP SRAM via both the data bus and instruction bus
  - 384 KB HP SRAM (0x4080_0000 ~ 0x4085_FFFF)
  - 16 KB LP SRAM (0x5000_0000 ~ 0x5000_3FFF)

- Direct access to modules/peripherals via the data bus, including:
```