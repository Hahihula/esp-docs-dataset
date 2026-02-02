**Title: Chapter 1 ULP Coprocessor (ULP)**

---

### Subtitle: JUMPS – Jump to a Relative Address (Conditional upon Stage Count Register)

#### Figure Caption:
- **Figure 1.4-9. Instruction Type — JUMP**

| Step | Description |
|------|-------------|
| 31   | Relative shift from current position, expressed in 32-bit words: <br> if Step[7] = 0, then PC = PC + Step[6:0] <br> if Step[7] = 1, then PC = PC - Step[6:0] |
| 28   | Threshold value for condition (see Cond below) to jump |
| 27   | Condition of jump: <br> 1X - jump if Stage_cnt <= Threshold <br> 0O - jump if Stage_cnt < Threshold <br> 0I - jump if Stage_cnt >= Threshold |

#### Note:
- A description of how to set the stage count register is provided in section **1.4.1.3**.
- All jump addresses are expressed in 32-bit words.

---

### Subtitle: HALT – End the Program

#### Figure Caption:
- **Figure 1.4-10. Instruction Type — HALT**

| Description |
|-------------|
| The instruction prompts a jump to a relative address if the above-mentioned condition is true. <br> The condition itself is the result of comparing the value of Stage_cnt (stage count register) and the Threshold value. |

---

### Subtitle: WAKE – Wake up the Chip

#### Figure Caption:
- **Figure 1.4-11. Instruction Type — WAKE**

| Description |
|-------------|
| After executing this instruction, the ULP coprocessor timer gets started.

---

**Footer Information:**  
Espressif Systems  
36  
ESP32 TRM (Version 5.6)  

**Link: Submit Documentation Feedback**