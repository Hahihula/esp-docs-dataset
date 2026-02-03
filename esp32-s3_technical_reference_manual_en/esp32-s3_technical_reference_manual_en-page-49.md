Title: Chapter 1 Processor Instruction Extensions (PIE)

Body Text:
However, if data is stored in memory at a non-aligned address, direct access to this address may cause it being split into two accesses, which in turn affects the performance of the code. For example, if you expect to read a 16-byte data from memory, as shown in Table 1.5-2, the data is stored in memory at OOOO when the data is aligned. But actually the data is not aligned, so the low nibble of its address may be any one between OOOO ~ 1111 (binary). Assuming the lowest bit of its address is O_0100, the processor will split the one-time access to this data into two accesses, i.e., to O_0000 and I_0000 respectively. The processor then put together the obtained two 16-byte data to get the required 16-byte data.

To avoid performance degradation caused by the above non-aligned access operations, all access addresses in the extended instruction set are forced to be aligned; i.e., the lowest bits will be replaced by O. For example, if a read operation is initiated for 128-bit data at Ox3fc8_0024, the lowest 4-bit of this access address will be forced to be set to O. Eventually, the 128-bit data stored at Ox3fc8_002O will be read. Similarly, the lowest 3-bit of the access address for 64-bit data will be set to O; the lowest 2-bit of the access address for 32-bit data will be set to O; the lowest 1-bit of the access address for 16-bit data will be set to O.

The above design requires aligned addresses of the access operations initiated. Otherwise, the data read will not be what you expected. In application code, you need to explicitly declare the alignment of the variable or array in memory. 16-byte alignment can meet the needs of most application scenarios.

The `aligned` (16) parameter declares that the variable is stored in a 16-byte aligned memory address. You can also request a data space with its starting address 16-byte aligned via heap_caps_aligned_alloc.

Since the memory address of the data involved in some operations is uncertain in specific application scenarios, this extended instruction set provides a special register SAR_BYTE and related instructions such as EE.LD.128.USAR.* and EE.SRC.*, to handle non-aligned data.

Assume that the 128-bit non-aligned data address is stored in the general-purpose register a8. This 128-bit data can be read into the specified QR register (q2 in the following example) by the following code:

```
EE.LD.128.USAR.IP q0, a8, 16
EE.VLD.128.IP q1, a8, 16
EE.SRC.Q q2, q0, I1
```

Subtitle: Data Overflow and Saturation Handling

Body Text:
Data overflow means that the size of the operation result exceeds the maximum value that can be stored in the result register. Take the EE.VMUL.S8 instruction as an example; the result of two 8-bit multipliers is 16-bit, and it should still be 16-bit after right-shifting. However, the final result will be stored in the 8-bit register, which may cause the risk of data overflow.

In the design of the ESP32-S3's instruction extensions, there are two ways to handle data overflow, namely taking saturation and truncating the least significant bit. The former controls the calculation result according the range of values that can be stored in the result register. If the result exceeds the maximum value of the result register, take the maximum value; if the result is smaller than the minimum value of the result register, take the minimum value. This approach will be explicitly indicated in the instruction descriptions. For example, the EE.VADDS.* instructions perform saturation to the results of addition operations. Regarding the data overflow handling for more instructions of their internal calculation results, the wraparound approach is used; i.e., only the lower bit of the result that is consistent with the bit width of the result register will be retained and stored in the result register.

Please note that for instructions that do not mention saturation handling method, the wraparound approach

Footer:
Espressif Systems
49 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback