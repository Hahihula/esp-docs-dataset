

```markdown
Chapter 5 System and Memory

GoBack

Figure 5.2-1. System Structure and Address Mapping

Note:
* The range of addresses available in the address space may be larger than the actual available memory of a particular type.
* For CPU Sub-system, please refer to Chapter 1 High-Performance CPU.

5.3 Functional Description

5.3.1 Address Mapping

All the non-reserved addresses are accessible by the instruction bus and the data bus, that is, the instruction bus and the data bus access the same address space.

Both data bus and instruction bus of the HP CPU and LP CPU are little-endian. The HP CPU and LP CPU can access data via the data bus using single-byte, double-byte, and 4-byte alignment.

The CPU can:
* directly access the internal memory via both data bus and instruction bus.
* (for HP CPU only) directly access the external memory which is mapped into the address space via cache.
* directly access modules/peripherals via data bus.
```