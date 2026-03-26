

Chapter 1 High-Performance CPU

4. Execute the application program.

5. During execution of the application code, if any PIE instruction is encountered, the `mext_pie_status.STATE` bits will automatically change to DIRTY (11).

During context switching, whether to save/restore the PIE extension registers can be decided based on the value of the `mext_pie_status.STATE` bits. If the value is DIRTY, the state of the PIE register must be saved to the stack. After that, the state would be updated to CLEAN or OFF, depending on whether the next context (thread) has the PIE extension enabled or not.

Some PIE instructions have constraints on the register fields or immediate fields. e.g. for fused instructions which are performing load and arithmetic, with the same destination register for the two parallel operations, it will be considered ambiguous and thus cause a PIE illegal exception with `mcause = 0x1f`.