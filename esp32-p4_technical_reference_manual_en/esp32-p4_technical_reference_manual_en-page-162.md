
```markdown
Chapter 1 High-Performance CPU

GoBack

1.12 Performance

1.12.1 Branch Prediction

1.12.1.1 Overview

A core does branch prediction in terms of branch is taken or not taken and the target address of conditional/unconditional branch type instruction prior to its execution. Based on the prediction, the core starts fetching from the respective PC. Then, it validates the prediction on the execution of the instruction. If it is found to be miss-predicted, then the core flushes the pipeline and starts fetching from the correct PC. The prediction improves the throughput as the core continues fetching instructions based on prediction instead of waiting till the execution of branch instruction. The details about the prediction technique used by the core are described in the following section.

1.12.1.2 Features

* Prediction of both results and target address of conditional/unconditional branch type instructions
* Branch target prediction of instructions including BEQ, BNE, BLT, BLTU, BGE, BGEU, C.BEQZ, C.BNEZ, JAL, J, CJ
* Conditional branch prediction includes instructions such as: BEQ, BNE, BLT, BLTU, BGE, BGEU, C.BEQZ, C.BNEZ
* Uses 2-bit saturating counter for more accuracy
* Uses global history of conditional branches for prediction which improves performance
* Target prediction in one clock cycle for unconditional branch, that is, 0 cycle penalty when prediction or speculation is correct

1.12.1.3 Functional Description

The core uses Branch History Table (BHT) along with Branch Target Buffer (BTB) for prediction of branch and jump type instructions.

BHT is 512x16-bit SRAM memory for each core. It is indexed by Virtual Branch History Register (VBHR) while performing prediction and by Global Branch History Register (GBHR) while updating or correcting the result (taken or not taken) on execution of branch-type instructions. GBHR contains the results of the last 13 branch-type instructions executed. VBHR contains the results of the last 12 branch-type instructions and predicted results of the current branch instruction. Thus, both registers hold the trajectory of previously executed branches. Based on 13 bits of VBHR and GBHR, 2 bits of saturation counter value stored in BHT are either read or written respectively.

As shown in Figure 1.12-1, 2-bit saturation counter indicates if a branch is:

* weakly not taken (00)
* strongly not taken (01)
* weakly taken (10)
* strongly taken (11)

Espressif Systems
```