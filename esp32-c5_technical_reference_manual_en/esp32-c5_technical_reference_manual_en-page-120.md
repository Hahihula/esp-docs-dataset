

```markdown
## 2.11 Performance

### 2.11.1 Branch Prediction

#### 2.11.1.1 Overview

A core does branch prediction in terms of whether a branch is taken or not taken and the target address of a conditional/unconditional branch type instruction prior to its execution. Based on the prediction, the core starts fetching from the corresponding PC. Then, it validates the prediction on the execution of the instruction. If the predication turns out to be incorrect, the core flushes the pipeline and starts fetching from the correct PC. Branch prediction improves the throughput by allowing the core to keep fetching instructions without waiting for the completion of earlier branch instructions. The details about the prediction technique used by the core are described in the following section.

#### 2.11.1.2 Features

- Prediction of both results and target address of conditional/unconditional branch type instructions
- Branch target prediction of instructions including BEQ, BNE, BLT, BLTU, BGE, BGEU, C.BEQZ, C.BNEZ, JAL, J, CJ
- Conditional branch prediction includes instructions such as: BEQ, BNE, BLT, BLTU, BGE, BGEU, C.BEQZ, C.BNEZ
- Uses 2-bit saturating counter for more accuracy
- Uses global history of conditional branches for prediction, which improves performance
- Target prediction in one clock cycle for unconditional branch, that is, 0 cycle penalty when prediction or speculation is correct

#### 2.11.1.3 Functional Description

The core uses the Branch History Table (BHT) along with the Branch Target Buffer (BTB) for prediction of branch and jump type instructions.

The BHT is a 512x16-bit SRAM used by the high-performance core for branch prediction. During prediction, it is indexed using the Virtual Branch History Register (VBHR). During update, after the branch resolves, the BHT is indexed using the Global Branch History Register (GBHR), which records the outcomes of the last 13 executed branches. VBHR contains the results of the last 12 branch-type instructions and the predicted results of the current branch instruction. Thus, both registers hold the trajectory of previously executed branches. Based on 13 bits of VBHR and GBHR, 2 bits of saturation counter value stored in BHT are either read or written, respectively.

As shown in Figure 2.11-1, 2-bit saturation counter indicates if a branch is:

- weakly not taken (00)
- strongly not taken (01)
- weakly taken (10)
- strongly taken (11)
```