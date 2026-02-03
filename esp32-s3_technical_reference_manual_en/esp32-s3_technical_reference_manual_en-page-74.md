**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Header:**
- EE.ZERO.Q — qa 1 — QACC_L, 1,
- EE.ZERO.QACC — — — QACC_H

**Section Heading:**
1.7.2 Hardware Resource Hazard

**Body Text:**
When multiple instructions call the same hardware resource at the same time, the processor allows only one of the instructions to occupy the hardware resource, and the rest of them will be delayed. For example, there are only eight 16-bit multipliers in the processor; instruction C requires eight of them in pipeline stage M, and instruction D requires four of them in pipeline stage E. As shown in Figure 1.7-2, instruction C is issued in cycle T+0, and instruction D is issued in cycle T+1, so four multipliers are applied to be occupied simultaneously in cycle T+3; at this time, the processor will delay the issue of instruction D into the pipeline by one cycle to avoid conflict with instruction C.

**Figure Description:**
- Figure 1.7-2 illustrates a timeline for hardware resource allocation.
- The diagram shows different cycles (T+0 through T+6) and whether Instruction C or Instruction D is in various states such as "R" (Ready), "E" (Executing), etc., indicating the occupation of multipliers.

**Subsection Heading:**
1.7.3 Control Hazard

**Body Text:**
Data and hardware resource hazards can be optimized by adjusting the code order, but the control hazard is difficult to optimize. Program code usually has many conditional select statements that execute different code depending on whether the condition is met or not. The compiler will process these above conditional statements into branch and jump instructions; if the condition is satisfied, it will jump to the target address to execute the corresponding code; if not, the subsequent instructions will be processed in order. When the conditions are met, as shown in Figure 1.7-3, the processor will re-fetch the instruction from the new target address. At this time, the instructions at the R and E stages on the pipeline will be removed, which means the pipeline remains stagnant for 2 cycles.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:** 
74