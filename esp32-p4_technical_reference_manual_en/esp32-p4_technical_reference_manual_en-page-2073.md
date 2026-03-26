

```markdown
Chapter 40  MIPI CSI                          GoBack


CSI_HOST_INT_FORCE_<group0>
[31 30 ... 1 0] (green box)

AND gates feeding into:
- group 0 interrupt source 0
- group 0 interrupt source 1
- ...
- group 0 interrupt source 30
- group 0 interrupt source 31

These feed into an AND gate that connects to:
CSI_HOST_INT_ST_<group0> (blue box, labeled "Clear on read access")

AND gates also connect from each interrupt source line through intermediate ANDs to the same main AND block.

Below that is:
CSI_HOST_INT_MSK_<group0> (blue box)

Repeating pattern for group31:

CSI_HOST_INT_FORCE_<group31>
[31 30 ... 1 0] (green box)

AND gates from:
- group 31 interrupt source 0
- ...
- group 31 interrupt source 31

Feed into ANDs that connect to:
CSI_HOST_INT_ST_<group31> ("Clear on read access")

AND gates also feed through intermediate logic.

Below is:
CSI_HOST_INT_MSK_<group31>

Final output from main AND blocks feeds into:
CSI_INTR (via final AND gate)

Figure 40.6-1. MIPI CSI Interrupt Mechanism
```