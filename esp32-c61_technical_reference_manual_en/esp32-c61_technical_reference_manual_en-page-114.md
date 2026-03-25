
```markdown
Chapter 1 ESP-RISC-V CPU

GoBack

1.11 Performance

1.11.1 Branch Prediction

1.11.1.1 Overview

A core does branch prediction in terms of branch is taken or not taken and the target address of conditional/unconditional branch type instruction prior to its execution. Based on the prediction, the core starts fetching from the corresponding PC. Then, it validates the prediction on the execution of the instruction. If the predication turns out to be incorrect, the core flushes the pipeline and start fetching from correct PC. Branch prediction improves the throughput by allowing the core to keep fetching instructions without waiting for the completion of earlier branch instruction. The details about the prediction technique used by the core are described in the following section.

1.11.1.2 Features

* Prediction of both results and target address of conditional/unconditional branch type instructions
* Branch target prediction of instructions including BEQ, BNE, BLT, BLTU, BGE, BGEU, C.BEQZ, C.BNEZ, JAL, J, CJ
* Conditional branch prediction includes instructions such as: BEQ, BNE, BLT, BLTU, BGE, BGEU, C.BEQZ, C.BNEZ
* Uses 2-bit saturating counter for more accuracy
* Uses global history of conditional branches for prediction which improves performance
* Target prediction in one clock cycle for unconditional branch, that is, 0 cycle penalty when prediction or speculation is correct

1.11.1.3 Functional Description

The core uses Branch History Table (BHT) along with Branch Target Buffer (BTB) for prediction of branch and jump type instructions. A 512x16-bit SRAM memory used for maintaining Branch History Table for HP core. During prediction, it is indexed by Virtual Branch History Register (VBHR). During update, after branch resolves, the BHT is indexed using Global Branch History Register (GBHR), which records the outcomes of the last 13 executed branch instructions. VBHR contains the results of the last 12 branch-type instructions and predicted results of the current branch instruction. Thus, both registers hold the trajectory of previously executed branches. Based on 13 bits of VBHR and GBHR, 2 bits of saturation counter value stored in BHT are either read or written respectively.

As shown in Figure 1.11-1, 2-bit saturation counter indicates if a branch is:

* weakly not taken (00)
* strongly not taken (01)
* weakly taken (10)
* strongly taken (11)

If the prediction result counter is in any not-taken state, the branch is predicted as not taken. Similarly, if the prediction result counter is in any taken state, the branch is predicted as taken. When the actual branch
```