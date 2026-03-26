

```markdown
If the result of prediction is weakly or strongly not taken, then the branch is predicted as not taken. Similar is the case for weakly/strongly taken.

While updating BHT with the actual result of branch execution, the following transition logic is used to update the respective saturation counter.

BTB stores the 32-bit branch target address. It can hold a maximum of 16 entries of target addresses. It is indexed by the last 16 bits of the PC of conditional/unconditional branch-type instruction. Thus, the core predicts the result of branch-type instructions based on BHT and jumps to the target obtained from BTB if the branch is predicted as taken. For unconditional branches, the core directly jumps to the target obtained from BTB, as it does not need prediction in this case. When the actual result and the target of branch-type instructions are obtained during execution, the core takes a corrective jump by flushing the pipeline in case of misprediction. BTB and BHT entries are corrected accordingly.

Figure 1.12-1 shows 2-bit saturation scheme details used in each HP core.
```

![Figure 1.12-1. Two-bit Saturation Counter](image_description)

```markdown
T: Taken
NT: Not Taken

## 1.12.2 RAS

### 1.12.2.1 Overview

Return Address Stack (RAS) is a stack maintained by the core to push the return addresses of jump and link (JAL/JALR) type instructions. Thus, the core can jump to the return address as soon as the RET instruction is pre-decoded, enhancing the performance of function call return.

### 1.12.2.2 Features

* Increased core performance by avoiding pipeline stall on return of function call
```