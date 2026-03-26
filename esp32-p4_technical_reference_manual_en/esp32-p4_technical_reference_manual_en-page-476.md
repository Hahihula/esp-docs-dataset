

```markdown
Chapter 7 System and Memory

GoBack

* LP SRAM (32 KB): A volatile memory accessible by both the HP CPU and LP CPU, operating at the same frequency as the LP CPU.
* HP SPM (8 KB): A volatile memory accessed by the HP CPU, finishing one access in two cycles.

1. Details for HP ROM

The 128 KB HP ROM is a read-only memory accessed by the HP CPU through the instruction bus or data bus via the following addresses as shown in Table 7.3-1:

* 0x4FC0_0000 (cache-able or noncache-able, configuration-dependent) ~ 0x4FC1_FFFF (cache-able or noncache-able, configuration-dependent).
* 0x8FC0_0000 (direct access by CPU) ~ 0x8FC1_FFFF (direct access by CPU).

2. Details for HP L2MEM

This 768 KB HP L2MEM is a read-and-write memory accessed by the HP CPU or LP CPU through the instruction bus or data bus, or by DMA master through AHB matrix or AXI matrix via the following addresses as shown in Table 7.3-1:

* 0x4FF0_0000 (cache-able or noncache-able, configuration-dependent) ~ 0x4FFB_FFFF (cache-able or noncache-able, configuration-dependent).
* 0x8FF0_0000 (direct access by CPU) ~ 0x8FFB_FFFF (direct access by CPU).

L2MEM supports multiple capacity split configurations: L2 RAM and L2 cache share a total capacity of 768 KB, and one of the following four configurations can be selected:

* Config 0: L2 RAM 256 KB, L2 cache 512 KB
* Config 1: L2 RAM 512 KB, L2 cache 256 KB
* Config 2: L2 RAM 640 KB, L2 cache 128 KB
* Config 3: L2 RAM 768 KB, L2 cache 0 KB

The address layout of HP L2MEM for the above four configurations is shown in Figure 7.3-2.
```