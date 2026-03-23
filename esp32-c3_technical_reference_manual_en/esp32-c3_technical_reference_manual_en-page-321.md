

```markdown
For example, if you want to split the instruction region at 0x3fc88000, then write the [16:9] bits of this address, which is Ob01000000, to SPLITADDR.

3. The split address applies to both IBUS and DBUS address. For example, DBUS address 0x3fc88000 and IBUS address 0x40388000 indicate the same location in SRAM1. The split address for both buses is [16:9].

| Internal SRAM 1 | Category0: 0x0 |
|-----------------|----------------|
| Block0          |                |
| Block1          | Category1: 0x1/0x2 |
|                 |                |
| Block2          | Category2: 0x3 |

Figure 14.4-2. An illustration of Configuring the Category fields

Note the following points when configuring the split lines:

* Position:
    - The split line that splitting the Instruction Region and Data Region can be configured anywhere inside Internal SRAM1.
    - The two split lines further splitting the Instruction Region into 3 split regions must stay inside the Instruction Region.
    - The two split lines further splitting the Data Region into 3 split regions must stay inside the Data Region.

* Split lines can overlap with each other. For example,
    - When the two split lines inside the Data Region are not overlapping with each other, then the Data Region is split into 3 split regions
    - When the two split lines inside the Data Region are overlapping with each other, then the Data Region is only split into 2 split regions
    - When the two split lines inside the Data Region are not only overlapping with each other but also with the split line that splits the Data Region and the Instruction Region, then the Data Region is not split at all and only has one region.

Access Configuration

After configuring the split lines, users can then use the registers described in the Table 14.4-6 and Table 14.4-7 below to configure the access of CPU’s IBUS, DBUS and GDMA peripherals, in the privileged environment and the unprivileged environment, to these split regions independently.
```