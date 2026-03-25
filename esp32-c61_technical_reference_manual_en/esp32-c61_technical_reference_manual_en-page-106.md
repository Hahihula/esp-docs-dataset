
```markdown
# 1.10.2 Hardware Trigger

## 1.10.2.1 Overview

HP core implements a hardware trigger block to provide breakpoint and watchpoint capability for debugging. It conforms to the [RISC-V External Debug Support Version 0.13.2 specification](#). Please refer to it for functional operation details.

### 1.10.2.2 Features

HP core trigger block support following features:

*   Three independent trigger units, each of which can be configured for matching the address of the program counter or load-store accesses
*   Preempting execution by causing a breakpoint exception
*   Halting execution and transferring control to debuggers
*   Support for NAPOT (naturally aligned power-of-two regions) address encoding

### 1.10.2.3 Functional Description

The Hardware Trigger module provides seven CSRs, which are listed under Section [register summary](#). Among these, `tdata1` and `tdata2` are abstract CSRs, which means they are shadow registers for accessing internal registers for each of the three trigger units, one at a time.

To choose a particular trigger unit write the index (0-2) of that unit into `tselect` CSR. When `tselect` is written with a valid index, the abstract CSRs `tdata1` and `tdata2` are automatically mapped to reflect internal registers of that trigger unit. Each trigger unit has two internal registers, namely `mcontrol` and `maddress`, which are mapped to `tdata1` and `tdata2`, respectively.

Writing larger than allowed indexes to `tselect` will clip the written value to the largest valid index, which can be read back. This property may be used for enumerating the number of available triggers during initialization or when using a debugger.

Since software or debugger may need to know the type of the selected trigger to correctly interpret `tdata1` and `tdata2`, the 4 bits (31-28) of `tdata1` encodes the type of the selected trigger. This type field is read-only and always provides a value of `0x2` for every trigger, which stands for match type trigger, hence, it is inferred that `tdata1` and `tdata2` are to be interpreted as `mcontrol` and `maddress`. The information regarding other possible values can be found in the specification, RISC-V External Debug Support Version 0.13, but this trigger module only supports type `0x2`.

Once a trigger unit has been chosen by writing its index to `tselect`, it will become possible to configure it by setting the appropriate bits in `mcontrol` CSR (`tdata1`) and writing the target address to `maddress` CSR (`tdata2`).

Each trigger unit can be configured to either cause breakpoint exception or enter debug mode, by writing to the action field of `mcontrol`. This bit can only be written from debugger, thus by default a trigger, if enabled, will cause breakpoint exception.

`mcontrol` for each trigger unit has a `hit` bit which may be read, after CPU halts or enters exception, to find out if this was the trigger unit that fired. This bit is set as soon as the corresponding trigger fires, but it has to be
```